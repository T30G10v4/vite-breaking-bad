<script>

    import axios from "axios";
    import AppWrapper from "./components/AppWrapper.vue";
    import AppCharacter from "./components/AppCharacter.vue";
    import AppCharactersList from "./components/AppCharactersList.vue";
    import { cards } from "./cards";

    export default {

        components: {

            AppWrapper,
            AppCharacter,
            AppCharactersList

        },
        data() {

            return {

                cards

            }

        },
        created() {

            this.cards.loading = true;
            axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {

                
                this.cards.characters = resp.data;
                console.log(this.cards.characters);
                this.cards.loading = false;

            });

        }

    }

</script>

<template>

</template>

<style lang="scss">
    @use "./styles/generals.scss" as *;
</style>
