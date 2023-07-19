<script>

    export default {
        data() {

            return {
                
            }

        },

        props: {

            card: {

                type: Object,

                default: {
                    archetype:'',
                    name:'',
                    card_images: ''
                }

            },
        }
       
    }

</script>

<template>

   <div class="card mb-3">

        <div class="card-img-top">
            <img :src="card.card_images[0].image_url" class="img-fluid" alt="">
        </div>

        <div class="card-body">

            <h2 class="card-title text-center text-white p-3">
                {{ card.name }}
            </h2>

            <h3 class="card-text text-center">
                {{ card.archetype }}
            </h3>
            
        </div>

    </div>

</template>

<style lang="scss" scoped>

</style>