<script>
import ItemNav from './Items/ItemNav.vue';

export default {
    name: 'AppHeader',

    components: {
        ItemNav,
    },

    data() {
        return {
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
                        'qualcosa',
                        'qualcosa',
                        'qualcosa',
                        'qualcosa',
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

                        'qualcosa',
                        'qualcosa',
                        'qualcosa',
                        'qualcosa',

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
                <!-- Qui creare v-for con prop -->
                <ul>
                    <!-- Qui creare elemento a se in components  -->
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
    background-color: $primary_white;
    color: $primary_color;


    .row-nav {

        display: flex;
        justify-content: space-between;
        align-items: center;
        
        .logo {

            width: 185px;
            padding: 25px 40px;

        }

        nav {
            flex-grow: 1;

            ul {
                display: flex;
                align-items: center;
                justify-content: center;
                gap: 40px;
                list-style-type: none;
            }    
        }

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
</style>./Items/ItemNav.vue