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
        <span>{{ TypeService.text }}</span>
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
    span {
        text-transform: uppercase;
        font-size: 14px;
        letter-spacing: 2px;
        font-weight: bold;
        color: $primary_color;
    }

    p {
        text-align: center;
        line-height: 30px;
        font-size: 16px;
        color: $secondary_color;
        font-family: "Roboto Condensed", sans-serif;
    }

}

</style>