<script>
import AppCharacter from './AppCharacter.vue';
import { cards } from "../cards";

export default {

    name: "AppCharactersList",
    components: {


            AppCharacter
    },
    data() {
        return {

            cards

        }


    }

}



</script>

<template>
    <div class="container">
        <div class="found">Found x Characters</div>
        <div class="row row-cols-xs-12 row-cols-md-5 gx-5">
            <AppCharacter v-for="character in cards.characters" :key="character.char_id" :character="character" />
        </div>
    </div>
</template>

<style lang="scss" scoped>

.container {

    background-color: white;
 

    .found {

        background-color: #212529;

    }

}

</style>
