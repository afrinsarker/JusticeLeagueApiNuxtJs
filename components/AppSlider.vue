<template>
  <div>
    <div
      id="carouselExampleControls"
      class="carousel slide"
      data-ride="carousel"
    >
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img
            style="opacity: 40%"
            src="https://c4.wallpaperflare.com/wallpaper/17/894/478/comics-justice-league-aquaman-batman-wallpaper-preview.jpg"
            class="d-block w-100"
            alt="..."
          />
          <div class="carousel-caption d-none d-md-block"></div>
        </div>
        <div class="carousel-item">
          <img
            style="opacity: 40%"
            src="https://i.pinimg.com/originals/3a/e0/83/3ae083a23be5bbd7b14c5e4c9592fd77.jpg"
            class="d-block w-100"
            alt="..."
          />
          <div class="carousel-caption d-none d-md-block"></div>
        </div>
      </div>
      <a
        class="carousel-control-prev"
        href="#carouselExampleControls"
        role="button"
        data-slide="prev"
      >
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a
        class="carousel-control-next"
        href="#carouselExampleControls"
        role="button"
        data-slide="next"
      >
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>
    <br />
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
</style>
