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
        <h3>{{ BlogArticles.title }}</h3>
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
        
        font-size: 10px;
        color: $secondary_color;
    }

    img {
        width: 100%;


    }

    h3 {
        text-transform: uppercase;
        font-size: 14px;
        color: $primary_color;
    }

    p {
        
        line-height: 25px;
        color: $secondary_color;
    }

}



</style>