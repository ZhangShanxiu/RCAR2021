<template>
  <div class="msg bg-white px-2" style="background-color:White;">
    <h1 style="margin-left:50px;">Committee</h1>
    <Committees />
  </div>
</template>

<script>
import Vue from "vue";
import Committees from "./../components/Committees.vue";
import { ImagePlugin } from "bootstrap-vue";
Vue.use(ImagePlugin);
export default {
  name: "CallForPapers",
  components: {
    Committees,
  },
};
</script>

<style>
.Committee {
  max-width: 1366px;
  margin:auto;
}
h1{
    color:rgb(28, 149, 206);
    font-family:Arial, Helvetica, sans-serif;
    font-weight: bold;
}
</style>