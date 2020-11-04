<template>
  <div class="modal-backdrop">
    <div class="modal">
      <header class="modal-header">
        <slot name="header">
          <button type="button" class="btn-close" @click="close">x</button>
        </slot>
      </header>
      <div class="modal-body">
        <slot name="body">
          <div class="cad-msg">
            Dana konfiguracja nie widnieje w tabeli CAD. Podaj numer wentylatora
            pod którym wybrana konfiguracja będzie widniała w tabeli CAD:
          </div>
        </slot>
      </div>
      <footer class="modal-footer">
        <slot name="footer">
          <div class="navi-btns"></div>
        </slot>
      </footer>
    </div>
  </div>
</template>

<script>
export default {
  name: "IfAdultModalComponent",
  data() {
    return {
      value: "",
      isCorrect: false,
    };
  },
  methods: {
    close() {
      this.$emit("close");
    },
  },
};
</script>

<style scoped>
</style>