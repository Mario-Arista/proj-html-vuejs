<script>

export default {
    name: 'ItemWork',

    props: {

        SingleWork: Array,

    },

}

</script>

<template>

    <div class="work">
        <div>
            <img :src="SingleWork.image" :alt="SingleWork.title">
        </div>
        <div class="title-work">{{ SingleWork.title }}</div>
        <span>{{ SingleWork.type }}</span>

    </div>

    

</template>

<style lang="scss">

@use '../../style/variables.scss' as *;


.work {
    position: relative;

    display: flex;
    flex-direction: column;
    align-items: center;

    width: calc(100% / 3 - 30px / 3 * 2);

    img {
        width: 100%;
        padding-bottom: 25px;

        cursor: pointer;

        &:hover {
            filter: grayscale(1.5);

        }

    }

    .title-work {
        text-transform: uppercase;
        font-size: 14px;
        font-weight: bold;
        color: $primary_color;
        padding-bottom: 20px;
    }

    span {
        text-align: center;
        font-size: 12px;
        color: $secondary_color;
        font-family: "Roboto Condensed", sans-serif;
    }

}



</style>