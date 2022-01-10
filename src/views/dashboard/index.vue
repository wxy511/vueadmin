<template>
  <div class="dashboard-container">
    <div class="dashboard-text">name: {{ name }}</div>
    <!-- <div>
      <ul v-for="set in sets">
        <li v-for="n in even(set)">{{ n }}</li>
      </ul>
    </div> -->
  </div>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  name: "Dashboard",
  // data() {
  //   return {
  //     sets: [
  //       [1, 2, 3, 4, 5],
  //       [6, 7, 8, 9, 10],
  //     ],
  //   };
  // },
  // methods: {
  //   even: function (numbers) {
  //     return numbers.filter(function (number) {
  //       return number % 2 === 0;
  //     });
  //   },
  // },
  computed: {
    ...mapGetters(["name"]),
  },
};
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
</style>
