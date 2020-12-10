<template>
  <div class="container">
    <div class="row">
      <div class="col-md-8">
        <p class="text-white mt-5">
          <span class="h1">Green Lantern</span><br />
        </p>
        <p class="text-white">
          <span class="h5">Biography :</span><br />
          Green Lantern first appeared in DC Comics' July 1940 edition of
          All-American Comics #16. He was created by Bill Finger and Martin
          Nodell. In 1941 the Green Lantern gained his own self titled comic
          book series.
        </p>
        <p class="text-white">
          <span class="h5">Super power :</span><br />
          The Green Lantern gains his super powers from his power ring. This
          ring can do almost anything depending on the strength of will of the
          user and his imagination. The Green Lantern has used this ring to fly,
          to create a green energy which can be used in a variety of ways, to
          hypnotize people, to become invisible, to translate languages, to pass
          through solid objects, to heal, to paralyze enemies, and even to time
          travel.
        </p>
      </div>
      <div class="col-md-4">
        <div class="card mt-5">
          <img
            class="card-img-top"
            src="https://static.wikia.nocookie.net/marvel_dc/images/c/cc/Aquaman_Vol_8_35_Textless.jpg/revision/latest?cb=20180418214425"
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
      console.log(response.data);
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
body {
  background-color: rgb(90, 90, 90);
}
</style>
