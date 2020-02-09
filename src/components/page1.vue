<template>
  <div>
    <h1>ここはページ１です。</h1>
    <router-link to="/page2">Go to page2</router-link>
    <div>
      <audio
        id="player1"
        autoplay
        controls
        src="/static/audio/kanpai.mp3"
        type="audio/mpeg"
      ></audio>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
let init = () => {
  document.addEventListener("click", audioPlay);
};

let audioPlay = () => {
  let player = document.getElementById("player1");
  player.play();
  document.removeEventListener("click", audioPlay);
};

init();
</script>

<style></style>
