<template>
  <div>
    <LotteryMainComponent></LotteryMainComponent>
  </div>
</template>

<script>
import LotteryMainComponent from "@/components/LotteryMainComponent.vue";

export default {
  name: "App",
  components: {
    LotteryMainComponent,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/main";
</style>
