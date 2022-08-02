<template>
  <div :class="{fadein: visible, hidden: !visible}">
    <slot></slot>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: false,
    }
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      if (!this.visible) {
        let top = this.$el.getBoundingClientRect().top;
        this.visible = top < window.innerHeight + 100;
      }
    }
  }
}
</script>

<style scoped>
.hidden {
  opacity: 0;
}

.fadein {
  animation: fadeIn 1s;
  opacity: 1;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
    transform: translateY(50px);
  }
  100% {
    opacity: 1;
  }
}
</style>