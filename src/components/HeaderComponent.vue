<script>

    export default {
        name: "HeaderComponent",
        data() {
            return {

            }
        },
        methods: {
            // funzione per le immagini:
            getImagePath: function(image){
                return new URL (image, import.meta.url).href;
            }
        },
        components: {
            
        },
        props:{
            
        },
    }

</script>

<template>

    <header>
        
        <div class="container-fluid">

            <div class="row">
                
                <div class="col-auto d-flex align-items-center">

                    <div class="logo_container">

                        <img class="img-fluid" src="../assets/img/logo.png" alt="yu_gi_logo">

                    </div>

                    <h1>
                        Yu-Gi-Oh Api
                    </h1>

                </div>

            </div>

        </div>

    </header>

</template>

<style lang="scss" scoped>

    @use "../assets/scss/partials/variables.scss" as *;


</style>