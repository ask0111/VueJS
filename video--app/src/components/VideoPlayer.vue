<template>
  <div>
<h1>{{video.name}}</h1>
    <video ref="videoPlayer" controls @timeupdate="updateSubtitle()">
      <source :src="video" type="video/mp4"/>
    </video>
  </div>
</template>

<script>
export default {
  props: {
    video: String
  },
  data(){
    return
  },
  methods: {
    updateSubtitle() {
      console.log(this.video, 'child')
      // Use this.$refs.videoPlayer.currentTime to update the subtitle display.
    },
  },
};
</script>

<style scoped>
video{
  width: 400px;
}
</style>