<script>

export default {
    name: 'ItemFooter',

    props: {

        Links: Array,

    },
}

</script>

<template>
    
    <ul id="footer-item">
        <li>
            <div class="title-footer"> {{ Links.title }}</div>
        </li>
        <li class="link-grey" v-for="CurrentLink in Links.voices"
        >
            {{ CurrentLink }} 
        </li>
    </ul>

</template>

<style lang="scss">

@use '../../style/variables.scss' as *;

#footer-item {

    li {

        list-style-type: none;
        text-decoration: none;


        &.link-grey {
        font-size: 14px;
        color: #cccccc;
        padding-bottom: 15px;
        }
    }
}

</style>