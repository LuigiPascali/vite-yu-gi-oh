<script>

  import HeaderComponent from './components/HeaderComponent.vue';
  import MainComponent from './components/MainComponent.vue';
  import Loader from './components/Loader.vue';

  import axios from 'axios';

  import {store} from './store'

  export default {

    data() {
      return {
        store,
        isLoading: false,
      }
    },
    methods: {

    },
    created() {
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
      .then(response => {
        
        this.store.cards = response.data.data;
        isLoading = true;
        
      })
    },

    components: {
      HeaderComponent,
      MainComponent,
      Loader
    }
  }

</script>

<template>

  <HeaderComponent />

  <Loader v-if="isLoading = false"/>

  <MainComponent v-else/>

</template>

<style lang="scss">

  @use "assets/scss/main";

</style>