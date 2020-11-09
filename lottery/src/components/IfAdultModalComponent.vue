<template>
  <div class="modal-backdrop">
    <div class="modal">
      <h2>Lottery</h2>

      <div class="enter-msg">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum
          doloremque, tempore debitis temporibus amet eum.
        </p>

        <div class="enter-name">
          <label>Enter your name player!</label>
          <input type="text" v-model="value" />
        </div>
      </div>

      <button type="button" class="btn-close" @click="close">Enter</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "IfAdultModalComponent",
  data() {
    return {
      value: "",
    };
  },

  methods: {
    close() {
      this.$emit("close", this.value);
    },
  },
};
</script>

<style scoped>
</style>






      