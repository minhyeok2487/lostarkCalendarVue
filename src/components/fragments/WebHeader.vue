<template>
  <div>
    <button v-on:click="getCategoryData">Button</button>
  </div>
</template>

<script>
import axios from "axios"
export default {
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