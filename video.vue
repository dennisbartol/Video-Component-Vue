<template>
  <div>
    <VideoStream :src="https://www.example.net./example.mp4" />
  </div>
</template>

<script>
  import VideoStream from './src/VideoStream.vue'; 

  export default { 
    name: 'App', 
    components: {
      VideoStream
    },
    data() {
      return { 
        videoSourceUrl: 'https://url.com/video.mp4'
      };
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
