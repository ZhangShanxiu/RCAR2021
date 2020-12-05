<template>
  <div class="ai-center d-flex jc-between py-2">
    <div class="logo">
      <img :src="logo" alt="" style="max-width:300px">
    </div>
    <span class="text text-right flex-1" >
      <h4>
        <b>2021 IEEE International Conference on Real-time</b>
      </h4>
      <h4>
        <b>Computing and Robotics</b>
      </h4>
      <h2 class="pt-3"><strong> July. 15-19, 2021, Xining, China</strong></h2>
    </span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      logo: require("./../../../src/logo/logo-flex2.png")
    };
  }
};
</script>

<style lang="scss">
.logo {
  float: left;
}
.text {
  float: right;
  font-size: 1.3em;
  font-weight: 600;
  // color: rgb(6, 17, 114);
  color: #3E99C9;
  margin-bottom: 0.5em;
  letter-spacing: .08em;
}
h4{
  font-family: Arial, Helvetica, sans-serif;
}

</style>