<template>
  <div class="lottery">
    <div class="neon-container">
      <div class="neon-text">
        <h1>Lottery! Check and win!</h1>
      </div>
    </div>

    <div class="lottery-informations">
      <div class="name-lottery-container">
        Witaj {{ user }}
        <!-- <button @click="openModal()">modal</button> -->
      </div>
      <div class="result-lottery-container">Poznaj wyniki</div>
    </div>
    <IfAdultModalComponent
      v-show="isModalVisible"
      @close="closeModal"
    ></IfAdultModalComponent>
  </div>
</template>

<script>
import IfAdultModalComponent from "@/components/IfAdultModalComponent.vue";

export default {
  name: "LotteryMainComponent",
  components: { IfAdultModalComponent },
  data() {
    return {
      user: "Mateusz",
      isModalVisible: false,
    };
  },
  methods: {
    openModal() {
      this.isModalVisible = true;
    },

    closeModal() {
      this.isModalVisible = false;
    },
  },
  beforeMount() {
    this.openModal();
  },
};
</script>


<style scoped lang="scss">
button {
  width: 100px;
  height: 30px;
}
</style>
