<script>

export default {
    name: "AppCharacter",
    props: {
        character: Object
    }
}

</script>

<template>

    <div class="my-card col">

        <img :src="character.img" alt="">
        <h2> {{character.name}}</h2>
        <h3>{{character.category}}</h3>
        <h4>{{character.status}}</h4>

    </div>

</template>

<style lang="scss" scoped>
    .my-card {

        background-color: #2e3a46;
        padding: 1rem;
        

    }

</style>
