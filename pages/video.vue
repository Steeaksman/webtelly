<template>

  <div class="min-h-screen  relative bg-cover bg-bottom  bg-fuchsia-900" >
  <!-- <div class="min-h-screen  relative bg-cover bg-bottom" style="background-image: url('https://tellysite.s3.us-west-1.amazonaws.com/RealBlue+Concert+background_2.jpg')"> -->
  <div class="p-8">
    <h1 class="text-2xl  mb-4 text-white">Make Me Rainbows</h1>
    <videoPlayer
      src="https://tellysite.s3.us-west-1.amazonaws.com/Make+me+rainbows.mp4"
      poster="https://tellysite.s3.us-west-1.amazonaws.com/thumbnailRainbows2.jpg"
      type="video/mp4"
    />
  </div>
  </div>
</template>

<script setup>
import VideoPlayer from '~/components/videoPlayer.vue'
</script>
