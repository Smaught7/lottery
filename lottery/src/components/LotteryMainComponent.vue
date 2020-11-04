<template>
  <div class="lottery">
    <div class="neon-container">
      <div class="neon-text">
        <h1>Lottery! Check and win!</h1>
      </div>
    </div>

    <div class="lottery-informations">
      <div class="name-lottery-container">Witaj Mateusz</div>
      <div class="result-lottery-container">Poznaj wyniki</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>


<style scoped lang="scss">
.neon-text {
  font-family: neon;
}
</style>
