<script>
import { cards } from "../cards";

export default {
    name: "AppWrapper",
    data() {

        return {

            cards


        }

    }
}

</script>

<template>

    <div class="container">

        <select @change="$emit(`selected`)" v-model="cards.series" class="form-select" aria-label="Default select example">
            <option selected value="">Open this select menu</option>
            <option value="Breaking Bad">Breaking Bad</option>
            <option value="Better Call Saul">Better Call Saul</option>
            
        </select>


    </div>


</template>

<style lang="scss" scoped>

</style>
