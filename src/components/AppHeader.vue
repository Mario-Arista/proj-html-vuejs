<script>

export default {
    name: 'AppHeader',
}

</script>

<template>
    <header>
        <div class="container">

            <!-- Logo Azienda  -->
            <img src="/img/logo.svg" alt="Logo Cinemato" class="logo">

            <!-- menu -->
            <nav>
                <!-- Qui creare v-for con prop -->
                <ul>
                    <!-- Qui creare elemento a se in components  -->
                    <li>Home</li>
                    <li>About</li>
                    <li>Ciao</li>
                    <li>Fine</li>
                    <li>Random</li>
                </ul>
            </nav>

            <!-- Search bar + social  -->
            <div id="right-part-header">

                <div class="search-bar">
                    <input type="text" class="hidden">
                    <img class="search-icon" src="/img/icon-search-thin.svg" alt="icona per cercare">
                </div>

                <div class="socials">
                    <img src="/public/img/icon-facebook.svg" alt="icona facebook">
                    <img src="/public/img/icon-twitter.svg" alt="icona facebook">
                    <img src="/public/img/icon-youtube.svg" alt="icona facebook">
                    <img src="/public/img/icon-instagram.svg" alt="icona facebook">
                </div>

            </div>

        </div>
        
    </header>
</template>

<style>

header {

    width: 100%;
    background-color: white;

    .container {

        display: flex;
        justify-content: space-between;
        align-items: center;
        
        .logo {

            width: 185px;
            padding: 25px 40px;

        }

        nav ul {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 40px;
            list-style-type: none;
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
</style>