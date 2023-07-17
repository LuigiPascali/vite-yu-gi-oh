<script>

    import SingleCard from './Card.vue';
    import {store} from '../store'

    export default {
        data() {
            return {
                store
            }
        },
        components: {
            SingleCard
        }
    }

</script>

<template>

    <main>

        <div class="container">

            <div class="py-4 row">

                <div class="col-auto">

                    <select class="form-select" aria-label="select">
                        <option selected> - </option>
                        <option value="1">Alien</option>
                        <option value="2">Noble Knight</option>
                        <option value="3">Tainted Treasure</option>
                        <option value="4">Melodious</option>
                        <option value="5">Archfiend</option>
                    </select>

                </div>

            </div>

            <div class="result bg-black px-5 py-3">
                <h3 class="text-white">
                    Found {{ store.cards.length }} cards
                </h3>
            </div>

            <div class="row">
                <div class="col-12 col-sm-6 col-md-5 col-lg-3" v-for="(card, i) in store.cards" :key="i">
                    <SingleCard :card="card" />
                </div>
            </div>

        </div>

    </main>

</template>

<style lang="scss" scoped>

    main {
        background-color: #D48F38;
    }

</style>