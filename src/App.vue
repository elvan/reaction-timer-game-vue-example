<template>
  <h1>Reaction Timer</h1>
  <button @click="start" :disabled="isPlaying">play</button>
  <Block v-if="isPlaying" :delay="delay" @end="endGame" />
  <p v-if="showResults">Reaction time: {{ score }} ms</p>
</template>

<script>
import Block from './components/Block';

export default {
  name: 'App',
  components: { Block },
  data() {
    return {
      isPlaying: false,
      delay: null,
      score: null,
      showResults: false,
    };
  },
  methods: {
    start() {
      // set time amount (ms)
      this.delay = 2000 + Math.random() * 5000;
      this.isPlaying = true;
      this.showResults = false;
    },
    endGame(reactionTime) {
      this.score = reactionTime;
      this.isPlaying = false;
      this.showResults = true;
    },
  },
};
</script>

<style>
#app {
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  margin-top: 60px;
  color: #444;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
}

button {
  margin: 10px;
  padding: 8px 16px;
  border: none;
  border-radius: 4px;
  color: white;
  font-size: 16px;
  letter-spacing: 1px;
  cursor: pointer;
  background: #0faf87;
}

button[disabled] {
  opacity: 0.2;
  cursor: not-allowed;
}
</style>
