<template>
  <video
    :id="playerId"
    ref="videoPlayer"
    class="video-js vjs-default-skin"
    controls
    preload="auto"
    :poster="poster"
    data-setup="{}"
  >
    <source :src="src" :type="type" />
    <p class="vjs-no-js">
      To view this video please enable JavaScript.
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
  playerId: { type: String, required: true } // ✅ each instance must be unique
})

const videoPlayer = ref(null)
let player = null

onMounted(() => {
  if (videoPlayer.value) {
    player = videojs(videoPlayer.value)
  }
})

onBeforeUnmount(() => {
  if (player) {
    player.dispose()
  }
})
</script>
