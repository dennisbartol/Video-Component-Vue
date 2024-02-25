
<template>
  <div>
    <VideoStream :src="http://#/example" />
  </div>
</template>

<script>
  import VideoStream from './VideoStream.vue'; 

  export default { 
    name: 'App', 
    components: {
      VideoStream
    },
    data() {

    }
  }
