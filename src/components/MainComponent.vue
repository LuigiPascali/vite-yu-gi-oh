<script>

    export default {
        name: "MainComponent",
        data() {
            return {

            }
        },
        methods: {

        },
        components: {
            
        },
        props:{
            
        },
    }
    
</script>

<template>

    <main>
        
        <div class="container">

            <div class="row py-4">

                <div class="col-auto">

                    <select class="form-select">

                        <option selected> Alien </option>

                    </select>

                </div>

            </div>

            <div class="row">

            </div>

        </div>

    </main>

</template>

<style lang="scss" scoped>

    @use "../assets/scss/partials/variables.scss" as *;

    main {
        background-color: #D48F38;
    }

</style>