<template>
  <div class="footer pt-5">
    <div class="col md-12 text-center text-white card bg-dark">
      Copyright @ Techminate2020
    </div>
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
/* Sticky footer styles
-------------------------------------------------- */
html {
  position: relative;
  min-height: 100%;
}
body {
  /* Margin bottom by footer height */
  margin-bottom: 60px;
}
.footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  /* Set the fixed height of the footer here */
  height: 60px;
  line-height: 60px; /* Vertically center the text there */
}
</style>
