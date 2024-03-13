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
            <img v-if="Menu.submenu" src="/public/img/icon-arrow-down.svg" alt="arrow-down icon">
        </div>
        <!-- VOCI NASCOSTE DEL SUBMENU, SE PRESENTE -->
        <div class="sub-nav" v-if="Menu.submenu">
            <a href="" class="voice-sub-menu" v-for="voice in Menu.submenu">{{ voice }}</a>
        </div>

    </li>

</template>

<style lang="scss" scoped>

// STYLE VOCI MENU

.voice-menu {
    position: relative;

    height: 100%;

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
.sub-nav {
    display: none;

    flex-direction: column;
    align-items: flex-start;

    position: absolute;
    top: 70px;
    z-index: 2;

    width: 250px;
    height: 150px;

    box-shadow: 0 2px 4px rgba(255, 255, 255, 0.319);

    background-color: black;


}

.voice-menu:hover + .sub-nav {
   display: flex;
}

.voice-sub-menu {
    display: flex;
    align-items: center;

    width: 100%;
    height: calc(100% / 3);

    border-bottom: 1px solid white;

    text-decoration: none;
    text-transform: uppercase;
    font-size: 12px;
    font-family: "Roboto Condensed", sans-serif;
    letter-spacing: 1px;
    font-weight: bold;

    color: white;
}

</style>