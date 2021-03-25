<template>
  <div style="width: 300px; margin: auto; padding-top: 50px;">
    <router-view name="header"></router-view>
    <transion
      name="fade"
      mode="out-in"
      @before-enter="beforeEnter"
    >
      <router-view></router-view>
    </transion>
  </div>
</template>

<script>
  export default {
    methods: {
      beforeEnter() {
        this.$root.$emit('triggerScroll');
      }
    }
  }
</script>

<style scoped>
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
</style>


