<!-- مشغل الموسيقى -->
<div class="music-player">
  <button id="musicBtn" onclick="toggleMusic()">🔊 تشغيل الموسيقى</button>

  <iframe
    id="musicFrame"
    width="0"
    height="0"
    src="https://www.youtube.com/embed/j9zuCKcYzhk?autoplay=0&loop=1&playlist=j9zuCKcYzhk"
    title="Music"
    allow="autoplay">
  </iframe>
</div>

<script>
let playing = false;

function toggleMusic(){
  const frame = document.getElementById("musicFrame");
  const btn = document.getElementById("musicBtn");

  if(!playing){
    frame.src =
      "https://www.youtube.com/embed/j9zuCKcYzhk?autoplay=1&loop=1&playlist=j9zuCKcYzhk";
    btn.innerHTML = "⏸ إيقاف الموسيقى";
    playing = true;
  }else{
    frame.src = "";
    btn.innerHTML = "🔊 تشغيل الموسيقى";
    playing = false;
  }
}
</script>
