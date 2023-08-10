<template>
<div>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <FileUpload v-on:fileToParent="updateFile($event)" />
  <VideoPlayer :video="file" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import FileUpload from './components/FileUpload.vue'
import VideoPlayer from './components/VideoPlayer.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    FileUpload,
    VideoPlayer
  },
  data(){
    return{
      file: 'data'
    }
  },
  methods:{
    updateFile(file){
      this.file = file;
      console.log(this.file, 'parent')
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
