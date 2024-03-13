<script>

export default {
    name: 'ItemArticleBlog',

    props: {

        BlogArticles: Array,

    },

}

</script>

<template>

    <div class="article">
        <img :src="BlogArticles.image" :alt="BlogArticles.title">
        <span>{{ BlogArticles.info }}</span>
        <div>{{ BlogArticles.title }}</div>
        <p>{{ BlogArticles.recap }}</p>
    </div>

</template>

<style lang="scss">

@use '../../style/variables.scss' as *;

.article {
    display: flex;
    flex-direction: column;
    gap: 15px 30px;

    width: calc(100% / 3 - 30px / 3 * 2);

    span {
        
        font-size: 12px;
        letter-spacing: 2px;
        color: $secondary_color;
        font-family: "Roboto Condensed", sans-serif;

    }

    img {
        width: 100%;


    }

    div {
        text-transform: uppercase;
        font-size: 14px;
        font-weight: bold;
        color: $primary_color;
    }

    p {
        
        line-height: 25px;
        color: $secondary_color;
        font-family: "Roboto Condensed", sans-serif;
        letter-spacing: 1px;
        font-size: 15px;
        text-align: justify;

    }

}



</style>