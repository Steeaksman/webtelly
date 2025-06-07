<template>
  <video
    ref="videoPlayer"
    class="video-js vjs-default-skin"
    controls
     width="900"
    height="506"
    preload="auto"
    :poster="poster"
    data-setup="{}"
  >
    <source :src="src" :type="type" />
    <p class="vjs-no-js">
      To view this video please enable JavaScript, and consider upgrading to a
      web browser that supports HTML5 video.
    </p>
  </video>
</template>

<script setup>
import { onMounted, onBeforeUnmount, ref } from 'vue'
import videojs from 'video.js'
import 'video.js/dist/video-js.css'

const props = defineProps({
  src: { type: String, required: true },
  type: { type: String, default: 'video/mp4' },
  poster: { type: String, default: '' },
})

const videoPlayer = ref(null)
let player = null

onMounted(() => {
  player = videojs(videoPlayer.value)
})

onBeforeUnmount(() => {
  if (player) {
    player.dispose()
  }
})
</script>
