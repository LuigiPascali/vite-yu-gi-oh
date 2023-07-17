<script>

    export default {

        name: "Card",

        data() {
            return {

            }
        },
        methods: {

        },
        components: {
            
        },
        props:{
           card: {
                type: Object,
                default: {
                    archetype: '',
                    name: '',
                    card_images: ''
                }
           } 
        },
    }

</script>

<template>

    <header>
        
        <div class="container-fluid">
            
            <div class="my_card">

                <div>
                    <img :src="card.card_images[0].image_url" class="img-fluid" alt="card_image">
                </div>

                <div>
                    <h3 class="text-center text-white p-4">
                        {{ card.name }}
                    </h3>
                </div>

                <div>
                    <h4 class="text-center">
                        {{ card.archetype }}
                    </h4>
                </div>

            </div>

        </div>

    </header>

</template>

<style lang="scss" scoped>

    @use "../assets/scss/partials/variables.scss" as *;


</style>