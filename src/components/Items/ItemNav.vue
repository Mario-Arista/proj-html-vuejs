<script>

export default {
    name: 'ItemNav',

    props: {

        Menu: Array,

    },
}

</script>

<template>

    
    <li>
        <div class="voice-menu">
            {{ Menu.title }}
            <img v-if="Menu.submenu"
             src="/public/img/icon-arrow-down.svg" alt="arrow-down icon">
        </div>

        <ul
            v-if="Menu.submenu"
        >
            <li class="voice-sub-menu"
                v-for="voice in Menu.submenu"
            >

                {{ voice }}

            </li>
        </ul>

    </li>

</template>

<style lang="scss" scoped>

.voice-menu {
    position: relative;
    text-transform: uppercase;
    font-size: 10px;
    font-weight: bold;

    img {
        position: absolute;
        bottom: -2px;
        right: -15px;
        width: 15px;
    }


}
.voice-sub-menu {
    display: none;
    text-transform: uppercase;
}

</style>