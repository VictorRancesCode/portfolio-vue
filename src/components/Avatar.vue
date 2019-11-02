<template>
  <img :class="`image-fluid img-header ${circle ? 'border-radius':''}`" :src="src" />
</template>
<script>
export default {
  name: "avatar",
  props: {
    circle: {
      type: Boolean,
      default() {
        return false;
      }
    },
    src: String
  }
};
</script>
<style scoped>
.img-header {
  width: 100%;
  transition: all 4s cubic-bezier(1, -0.53, 0.405, 1.425);
}
.border-radius {
  width: 80%;
  border-radius: 50%;
}
</style>