<script>

export default {
    name: 'ItemNav',

    props: {

        Menu: Array,

    },
}

</script>

<template>

    <!-- VOCI MENU PRINCIPALE -->
    <li>
        <div class="voice-menu">
            {{ Menu.title }}
            <img v-if="Menu.submenu"
             src="/public/img/icon-arrow-down.svg" alt="arrow-down icon">
        </div>

         <!-- VOCI NASCOSTE DEL SUBMENU, SE PRESENTE -->
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

// STYLE VOCI MENU
.voice-menu {
    position: relative;
    text-transform: uppercase;
    font-size: 12px;
    font-weight: bold;
    font-family: "Roboto Condensed", sans-serif;
    letter-spacing: 1px;

    img {
        position: absolute;
        bottom: -2px;
        right: -15px;
        width: 15px;
    }


}

// STYLE VOCI SUBMENU

.voice-sub-menu {
    display: none;
    text-transform: uppercase;
    font-size: 12px;
    font-family: "Roboto Condensed", sans-serif;
    letter-spacing: 1px;
}

</style>