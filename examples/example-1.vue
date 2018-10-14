<template>
    <div>
      <span class="pin">passed thing: {{passed}}</span>
      
      <div class="scroll-mark">scroll!</div>
      
      <div class="scroll-mark">keep scrolling!</div>
      
      <VueVisibilityTrigger class="highlight" @scrolledIn="logStatus" />
      
      <div class="scroll-mark">scroll back!</div>
    </div>
</template>

<script>
import VueVisibilityTrigger from "../src/vue-visibility-trigger.vue";
export default {
  name: "Example1",
  data() {
    return {
      passed: false
    };
  },
  methods: {
    logStatus(e) {
      this.passed = e;
      e ? console.log("PASSED") : console.log("WENT BACK");
    }
  },
  components: {
    VueVisibilityTrigger
  }
};
</script>

<style>
.pin {
  position: fixed;
  top: 0;
  z-index: 999;
  width: 100%;
  height: 23px;
}
.scroll-mark {
  width: 100px;
  margin: 400px auto;
  text-align: center;
}
.highlight {
  display: block;
  padding: 50px 0;
  text-align: center;
  background-color: rgba(0, 255, 0, 0.4);
}
.highlight:before {
  content: "thing";
}
</style>