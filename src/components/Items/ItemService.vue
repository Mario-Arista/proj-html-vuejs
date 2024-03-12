<script>

export default {
    name: 'ItemService',

    props: {

        TypeService: Array,

    },

}

</script>

<template>

    <div class="service">
        <img :src="TypeService.image" :alt="TypeService.text">
        <h3>{{ TypeService.text }}</h3>
        <p>{{ TypeService.description }}</p>
    </div>

</template>

<style lang="scss">

@use '../../style/variables.scss' as *;

.service {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 30px;

    width: calc(100% / 3 - 100px / 3 * 2);

    img {
        max-width: 80px;
        height: 80px;

    }
    h3 {
        text-transform: uppercase;
        font-size: 14px;
        color: $primary_color;
    }

    p {
        text-align: center;
        line-height: 25px;
        color: $secondary_color;
    }

}

</style>