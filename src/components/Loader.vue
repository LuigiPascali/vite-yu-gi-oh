<script>

    import {store} from '../store.js'

    export default {
        
        data() {
        return{
            store,
        }
        },
        methods: {
            
        },
        components: {
            
        },
        props:{
            
        }
        
    }

</script>


<template>

    <div class="loader">
      <div class="loader-inner"></div>
    </div>

</template>
  
<style lang="scss" scoped>

    .loader {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100px;
    }

    .loader-inner {
        display: inline-block;
        width: 20px;
        height: 20px;
        border-radius: 50%;
        background-color: #3498db;
        animation: loaderAnimation 1s infinite ease-in-out;
    }

    @keyframes loaderAnimation {
        0% {
            transform: scale(1);
            background-color: #3498db;
        }
        50% {
            transform: scale(1.5);
            background-color: #e74c3c;
        }   
        100% {
            transform: scale(1);
            background-color: #3498db;
        }
    }

</style>