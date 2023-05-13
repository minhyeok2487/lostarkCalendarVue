<template>
  <div>
    {{ message }}
    <button v-on:click="getCategoryData">Button</button>
  </div>
</template>

<script>
import axios from "axios"

export default {
  data() {
    return {
      message: ""
    }
  },
  methods: {
    getCategoryData() {
      axios.get("http://igdb.kro.kr/lostark/api/getMyCharacter")
      .then((res) => {
        console.log(res.data);
      })
      .catch((err) => {
        console.log(err);
      });
    }
  }
}
</script>

<style>

</style>