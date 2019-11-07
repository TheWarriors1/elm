<template>
  <div id="app">
    <p class="h2">16px</p>
    <p class="h3">24px</p>
    <p class="h4">甜品36px</p>
    <router-view />
    <vue1></vue1>
  </div>
</template>

<script>
import vue1 from "./components/vue1";
export default {
  components: {
    vue1
  },
  created() {
    window.onload = function() {
      document.documentElement.style.fontSize =
        (document.documentElement.clientWidth / 1080) * 100 + "px";
      window.onresize = function() {
        document.documentElement.style.fontSize =
          (document.documentElement.clientWidth / 1080) * 100 + "px";
      };
    };
  }
};
</script>

<style>
.h2 {
  font-size: 0.16rem;
}
.h3 {
  font-size: 0.24rem;
}
.h4 {
  font-size: 0.36rem;
}
</style>

