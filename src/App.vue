<template>
  <div class="app">
    <MyComponent/>
  </div>
</template>

<script>
import MyComponent from "./components/MyComponent.vue";

export default {
  name: "App",
  components: {
    MyComponent
  }
};
</script>

<style lang="scss">
.app {
  color: #2c3e50;
  margin-top: 60px;
}
</style>
