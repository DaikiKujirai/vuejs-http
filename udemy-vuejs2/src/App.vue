<template>
  <div class="main">
    <button @click="show = !show">切り替え</button>
    <transition name="fade">
    <p v-if="show">hello</p>
    </transition>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: true
    };
  }
};
</script>

<style scoped>
.fade-enter {
  opacity: 1;
}
.fade-enter-active {
  transition: opacity 0.5s;
}
.fade-enter-to {
  opacity: 0;
}
.fade-leave {
  opacity: 0;
}
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-leave-to {
  opacity: 1;
}

.main {
  width: 70px;
  margin: auto;
  padding-top: 5rem;
  text-align: center;
}
</style>script