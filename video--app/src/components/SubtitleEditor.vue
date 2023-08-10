<template>
  <div>
    <textarea v-model="subtitleText"></textarea>
    <button @click="addSubtitle">Add Subtitle</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      subtitleText: "",
    };
  },
  methods: {
    addSubtitle() {
      // Use a method to send the subtitle text and timestamp to the parent component.
      this.$emit("subtitle-added", {
        text: this.subtitleText,
        timestamp: // get the current video timestamp,
      });
      this.subtitleText = "";
    },
  },
};
</script>
