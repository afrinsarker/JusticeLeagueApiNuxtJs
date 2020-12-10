<template>
  <div class="container">
    <AppSlider />
    <HeroGrid />
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Justice League",
      meta: [
        {
          hid: "Justice League",
          name: "Justice League",
          content: "Justice League",
        },
      ],
    };
  },
};
</script>

<style>
body {
  background-color: rgb(90, 90, 90);
}
</style>
