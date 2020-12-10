<template>
  <div class="row">
    <div class="col-md-3 mt-2" v-for="hero in characters" v-bind:key="hero.id">
      <div class="card">
        <nuxt-link :to="'/' + hero.id">
          <img
            class="card-img-top"
            :src="'https://justiceleagueheros.herokuapp.com' + hero.image"
            alt="Card image"
            style="width: 100%"
          />
          <div class="card-body">
            <h4 class="card-title">{{ hero.name }}</h4>
          </div>
        </nuxt-link>
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
      characters: [],
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
        "https://justiceleagueheros.herokuapp.com/api/characters/",
        config
      );
      this.characters = response.data;
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
</style>
