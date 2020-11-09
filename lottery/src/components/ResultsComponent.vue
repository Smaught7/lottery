<template>
  <div class="result-view">
    <h2>Check results</h2>
    <ul class="result-list">
      <li v-for="result in results" :key="result.id">
        Lucky numbers: {{ result.numbers }}
      </li>
    </ul>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "resultsComponent",
  data() {
    return {
      results: [],
    };
  },

  async mounted() {
    try {
      let result = await axios({
        method: "POST",
        url: "https://www.lottohelden.de/graphql",
        data: {
          query: `
            {
                ticketNumber(type: "") {
                    numbers
                }
            }
            `,
        },
      });

      this.results = result.data.data.ticketNumber;
    } catch (error) {
      console.error(error);
    }
  },
};
</script>