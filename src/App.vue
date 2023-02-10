<template>
  <h1>Reaction Timer Game</h1>

  <button :disabled="isPlaying" @click="startGame">Play</button>

  <Block v-if="isPlaying" :delay="delay" @end="endGame" />

  <Results v-if="showResults" :score="score" />
</template>

<script>
import Block from './components/Block.vue';
import Results from './components/Results.vue';

export default {
  components: {
    Block,
    Results,
  },

  data() {
    return {
      isPlaying: false,
      delay: 0,
      score: 0,
      showResults: false,
    };
  },

  methods: {
    startGame() {
      this.showResults = false;
      this.delay = 2000 + Math.random() * 3000;
      this.isPlaying = true;
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
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #444;
  margin-top: 60px;
}

button {
  background: #0faf87;
  color: white;
  border: none;
  padding: 8px 16px;
  border-radius: 4px;
  font-size: 16px;
  letter-spacing: 1px;
  cursor: pointer;
  margin: 10px;
}

button[disabled] {
  opacity: 0.2;
  cursor: not-allowed;
}
</style>
