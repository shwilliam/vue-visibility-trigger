<script>
export default {
  name: "VueVisibilityTrigger",
  data() {
    return {
      showing: false
    };
  },
  methods: {
    checkNodeVisibility() {
      const { scrollY, innerHeight } = window;
      const isShowing = scrollY + innerHeight > this.$el.offsetTop;

      if (isShowing !== this.showing) {
        this.$emit("scrolledIn", isShowing);
        this.showing = isShowing;
      }
    }
  },
  created() {
    window.addEventListener("scroll", this.checkNodeVisibility);
    window.addEventListener("resize", this.checkNodeVisibility);
  },
  destroyed() {
    window.removeEventListener("scroll", this.checkNodeVisibility);
    window.removeEventListener("resize", this.checkNodeVisibility);
  }
};
</script>

<template>
  <span/>
</template>
