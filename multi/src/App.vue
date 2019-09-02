<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <br />
    <input v-model="num" />
    <Counter
      v-for="n in getNumber()"
      v-bind:key="n"
      v-bind:counter="n"
      v-bind:index="n"
      v-on:update="sum += $event"
    />
    sum:{{sum}}
  </div>
</template>

<script>
import Counter from "./components/Counter.vue";
export default {
  name: "app",
  components: {
    Counter
  },
  data() {
    return {
      num: 0,
      sum: 0
    };
  },
  methods: {
    getNumber: function() {
      if (this.isNumber(this.number)) {
        return parseInt(this.number);
      } else {
        return 0;
      }
    },
    isNumber: function(n) {
      return !isNaN(parseFloat(n)) && isFinite(n);
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
