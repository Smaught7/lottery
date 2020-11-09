<template>
  <div class="lottery">
    <div class="neon-container">
      <div class="neon-text">
        <h1>Lottery! Check and win!</h1>
      </div>
    </div>

    <div class="lottery-informations">
      <div class="name-lottery-container">
        <div class="user-name" v-if="value == ''">Hello {{ anonimous }}</div>
        <div class="user-name" v-else>Hello {{ value }}</div>
      </div>
      <div class="result-lottery-container">
        <ResultsComponent />
      </div>
    </div>
    <IfAdultModalComponent
      v-show="isModalVisible"
      @close="closeModal"
    ></IfAdultModalComponent>
  </div>
</template>

<script>
import IfAdultModalComponent from "@/components/IfAdultModalComponent.vue";
import ResultsComponent from "@/components/ResultsComponent.vue";

export default {
  name: "LotteryMainComponent",
  components: { IfAdultModalComponent, ResultsComponent },
  data() {
    return {
      value: "",
      anonimous: "User",
      isModalVisible: false,
    };
  },
  methods: {
    openModal() {
      this.isModalVisible = true;
    },

    closeModal(params) {
      this.isModalVisible = false;
      this.value = params;
    },
  },

  beforeMount() {
    this.openModal();
  },
};
</script>


<style scoped lang="scss">
</style>
