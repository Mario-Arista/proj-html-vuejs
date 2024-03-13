<script>
import ItemNav from './Items/ItemNav.vue';

export default {
    name: 'AppHeader',

    components: {
        ItemNav,
    },

    data() {
        return {

            // ARRAY PER POPOLARE NEL ITEMNAV LE VODI DEL MENU E SUBMENU
            navLinks: [
                {
                    title: 'home',
                },
                {
                    title: 'blog',
                },
                {
                    title: 'pages',
                    submenu: [
                        'SEVICES',
                        'OUR WORK FLOW',
                        'VIDEO THUMNAIL TYPE',
                    ],
                },
                {
                    title: 'about',
                },
                {
                    title: 'contacts',
                },
                {
                    title: 'gallery',
                },
                {
                    title: 'shop',
                    submenu: [

                    'RENT EQUIPMENT',
                    'CONSULTING',
                    'VIDEO ADS',

                    ]
                },

            ]
        }
    }
}

</script>

<template>

    <header>
        
        <div class="row-nav">

            <!-- Logo Azienda  -->
            <img src="/img/logo.svg" alt="Logo Cinemato" class="logo">

            <!-- menu -->
            <nav>
                
                <ul>
                    <!-- elemento ITEM NAV  -->
                    <ItemNav 
                        v-for="currentLink in navLinks"
                        :Menu="currentLink"
                    >
                    </ItemNav>
                </ul>
            </nav>

            <!-- Search bar + social  -->
            <div id="right-part-header">

                <div class="search-bar">
                    <input type="text" class="hidden">
                    <img class="search-icon" src="/img/icon-search-thin.svg" alt="icona per cercare">
                </div>

                <div class="socials">
                    <img src="/img/icon-facebook.svg" alt="icona facebook">
                    <img src="/img/icon-twitter.svg" alt="icona facebook">
                    <img src="/img/icon-youtube.svg" alt="icona facebook">
                    <img src="/img/icon-instagram.svg" alt="icona facebook">
                </div>

            </div>

        </div>
        
    </header>
    
</template>

<style lang="scss">

@use '../style/variables.scss' as *;

header {

    width: 100%;
    height: 70px;
    background-color: $primary_white;
    color: $primary_color;


    .row-nav {

        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;
        

        .logo {

            width: 185px;
            padding: 25px 40px;

        }

        // STILE NAV CON ITEM

        nav {
            flex-grow: 1;

            ul {
                display: flex;
                align-items: stretch;
                justify-content: center;
                gap: 40px;
                list-style-type: none;

                height: 100%;
            }    
        }

        // PARTE CON SOCIAL AND SEARCH
        #right-part-header {

            display: flex;
            align-items: center;
            gap: 20px;

            padding-right: 50px;

            .search-bar {

                display: flex;
                gap: 20px;
                border-right: 1px solid black;

                img {
                    height: 20px;
                    padding-right: 20px;
                }

            }

            .socials {
                display: flex;
                gap: 20px;

                img {
                    height: 15px;
                    width: 15px;
                }
            }
        }

    }
            
        
}
</style>