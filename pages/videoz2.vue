<template>
  <div class="grid gap-8 p-8">
    <videoPlayer
      player-id="video-1"
      src="https://hburg.s3.us-west-1.amazonaws.com/Daddy+Benny+Concert2.mp4"
      poster="/images/thumb1.jpg"
    />
    <videoPlayer
      player-id="video-2"
      src="https://hburg.s3.us-west-1.amazonaws.com/Bennys+Solo.mp4"
      poster="/images/thumb2.jpg"
    />
    <videoPlayer
      player-id="video-3"
      src="https://hburg.s3.us-west-1.amazonaws.com/Daddy+Benny+Concert2.mp4"
      poster="/images/thumb3.jpg"
    />
  </div>
</template>

<script setup>
import videoPlayer from '~/components/videoPlayerM.vue'

</script>


