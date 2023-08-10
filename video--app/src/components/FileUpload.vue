<template>
  <div>
    <input type="file" @change="uploadFile" />
  </div>
</template>

<script>
export default {
    name: "FileUpload",
    data()
    {
        return {
             file: {}
        }
    },
  methods: {
    async uploadFile(event) {
      this.file = event.target.files[0];
      const url = URL.createObjectURL(this.file)
      console.log(this.file)
      this.$emit('fileToParent', url)
      
    }
  },
};
</script>
