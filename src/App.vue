<template>
  <div class="">
    <!-- NAVIGATION BAR -->
    <Navigation></Navigation>
    <!-- NAVIGATION BAR -->
    <div>
      <router-view />
    </div>
  </div>
</template>

<script>
  import Navigation from './components/Navigation';

  export default {
    name: 'App',

    components: {
      Navigation,
    },

    data() {
      return {


      }
    },
    created() {
      // console.log("path", this.$route.path)
    },
  };
</script>
<style lang="scss">
  @import "./sass/main.scss";
</style>