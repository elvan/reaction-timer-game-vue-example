<template>
  <h1>Reaction Timer Game</h1>

  <button :disabled="isPlaying" @click="start">Play</button>

  <Block v-if="isPlaying" :delay="delay" />
</template>

<script>
import Block from './components/Block.vue';
export default {
  components: {
    Block,
  },

  data() {
    return {
      isPlaying: false,
      delay: 0,
    };
  },

  methods: {
    start() {
      this.delay = 2000 + Math.random() * 5000;
      this.isPlaying = true;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #444;
  margin-top: 60px;
}
</style>
