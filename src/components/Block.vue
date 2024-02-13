<template>
  <div class="block" v-show="showBlock" @click="stopTimer">click me</div>
</template>

<script>
export default {
  props: ['delay'],
  data() {
    return {
      showBlock: false,
      timer: null,
      reactionTime: 0,
    };
  },
  mounted() {
    setTimeout(() => {
      this.showBlock = true;
      this.startTimer();
    }, this.delay);
  },
  methods: {
    startTimer() {
      // start the timer, tick every 10ms
      this.timer = setInterval(() => {
        this.reactionTime += 10;
      }, 10);
    },
    stopTimer() {
      // stop the timer
      clearInterval(this.timer);
      console.log(this.reactionTime);
    },
  },
};
</script>

<style>
.block {
  width: 400px;
  margin: 40px auto;
  padding: 100px 0;
  border-radius: 20px;
  color: white;
  text-align: center;
  background: #0faf87;
}
</style>
