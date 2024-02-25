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
      const video = this.$reds.videoPlayer;
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

body { 
  margin: 0; 
  padding: 0; 
  min-height: 100vh; 
  background-color: #010101; 
  color: ghostwhite; 
}

  
</style> 
