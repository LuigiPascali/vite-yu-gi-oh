<script>

  import HeaderComponent from "./components/HeaderComponent.vue";
  import MainComponent from "./components/MainComponent.vue";

  import axios from "axios";

  export default {

    name: "App",

    components: {
      HeaderComponent,
      MainComponent,
    },

    data() {
      return {};
    },

    methods: {

    },

    created() {
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
      .then(response => {
        console.log(response.data)
      })
    },
    
  };

</script>

<template>

  <HeaderComponent />

  <MainComponent />

</template>

<style lang="scss">

  @use "assets/scss/main";

</style>