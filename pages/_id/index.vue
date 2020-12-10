<template>
  <div class="container">
    <div class="row">
      <div class="col-md-8">
        <p class="text-white mt-4">
          <span class="h1">{{ character.name }}</span
          ><br />
        </p>
        <p class="text-white">
          <span class="h5">Biography : </span><br />
          {{ character.bio }}
        </p>
        <p class="text-white">
          <span class="h5">Super power :</span><br />
          {{ character.special_power }}
        </p>
      </div>
      <div class="col-md-4">
        <div class="card mt-5">
          <img
            class="card-img-top"
            v-if="loaded"
            :src="'https://justiceleagueheros.herokuapp.com' + character.image"
            alt="Card image"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  components: {},
  data() {
    return {
      loaded: false,
      character: {},
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json",
      },
    };
    try {
      const response = await axios.get(
        `https://justiceleagueheros.herokuapp.com/api/character-detail/ 
          ${this.$route.params.id}`,
        config
      );
      this.character = response.data;
      this.loaded = true;
    } catch (error) {
      console.log(error);
    }
  },

  methods: {},
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
