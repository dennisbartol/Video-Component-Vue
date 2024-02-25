<template>
  <div class="video-stream">
    <video ref="videoPlayer" controls></video>
  </div>
</template>

<script>
  
  export default { 
    name: 'VideoStream', 
    props: {
      src: {
        type: String, 
        required: true
      }
    },
  mounted() {
    this.setupPlayer();
  },
  methods: {
    setupPlayer() {
      const video = this.$refs.videoPlayer;
      video.src = this.src; 
      video.addEventListener('loadedmetadata', this.playVideo);
    },

  playVideo() {
      const video = this.$refs.videoPlayer;
      video,.play();
      }
   },
    beforeUnmount() { 
      const video = this.$refs.videoPlayer; 
      video.removeEventListener('loadedmetadata', this.playVideo);
    }
};
     
</script>


<style>

.video-stream { 
    width: 100%; 
    max-width: 800px; 
    margin: 0 auto;
}
  
</style> 
