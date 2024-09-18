<template>
  <div class="layout">
    <Header />
    <div style="padding: 20px;">
      <slot />
    </div>
  </div>
</template>

<script>
import Header from "../components/Header.vue";

export default {
  components: {
    Header,
  },
};
</script>


<style>
</style>
