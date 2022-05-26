<template>
  <div>
    <FlashingMessage :delay="500" message="Hello friends!" />
    <!--  <TimerTest :delay="2000" name="Timer 1" @tick="onTick" />
    <TimerTest :delay="4000" name="Timer 2" @tick="onTick" />
    <LifecycleTest
      v-if="numberOfClicks < 10"
      :number-of-clicks="numberOfClicks"
    /> 
    <CongratulationsMsg
      :number-of-clicks="numberOfClicks"
      :current-date="currentDate"
    />
    <CounterButton
      :number-of-clicks="numberOfClicks"
      @increment="increment"
      @reset="reset"
    />
    <PeopleList />-->
  </div>
</template>

<script>
import PeopleList from "./components/PeopleList.vue";
import CounterButton from "./components/CounterButton.vue";
import CongratulationsMsg from "./components/CongratulationsMsg.vue";
import LifecycleTest from "./components/LifecycleTest.vue";
import TimerTest from "./components/TimerTest.vue";
import FlashingMessage from "./components/FlashingMessage.vue";

export default {
  name: "App",
  components: {
    FlashingMessage,
    PeopleList,
    CounterButton,
    CongratulationsMsg,
    LifecycleTest,
    TimerTest,
  },
  data() {
    return {
      numberOfClicks: 0,
      currentDate: new Date().toISOString(),
    };
  },
  methods: {
    increment() {
      return this.numberOfClicks++;
    },
    reset() {
      this.numberOfClicks = 0;
      return this.numberOfClicks;
    },
    onTick(name) {
      console.log(`Tick ${name}!`);
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
  color: #2c3e50;
  margin-top: 60px;
}
</style>
