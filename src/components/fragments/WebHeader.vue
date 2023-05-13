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
      axios.get("https://172.30.1.51:8080/lostark/api/getMyCharacter")
      .then((res) => {
        this.message = res.data;
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