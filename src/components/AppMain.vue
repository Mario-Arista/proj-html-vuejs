<script>

import SectionAboutUS from './Sections/SectionAboutUS.vue';
import SectionNumbers from './Sections/SectionNumbers.vue';
import SectionTeam from './Sections/SectionTeam.vue';
import SectionQuotes from './Sections/SectionQuotes.vue';
import SectionBlog from './Sections/SectionBlog.vue';
import SectionIcons from './Sections/SectionIcons.vue';

import ItemService from './Items/ItemService.vue';
import ItemWork from './Items/ItemWork.vue';

export default {
    name: 'AppMain',

    components: { 

        SectionAboutUS, 
        SectionNumbers,
        SectionTeam,
        SectionQuotes,
        SectionBlog,
        SectionIcons,

        ItemService,
        ItemWork, 
    },

    data() {
        return {
            services: [
                {
                    image: '/img/service-1.svg',
                    text: 'Array of equipment',
                    description: 'Lorem ipsum amet, consectetur adipiscing. Pallentesque ultriecies justo tellus.',

                },
                {
                    image: '/img/service-2.svg',
                    text: 'New tecnologies',
                    description: 'Lorem ipsum amet, consectetur adipiscing. Pallentesque ultriecies justo tellus.',

                },
                {
                    image: '/img/service-3.svg',
                    text: 'Versatile Actors',
                    description: 'Lorem ipsum amet, consectetur adipiscing. Pallentesque ultriecies justo tellus.',

                },
                {
                    image: '/img/service-4.svg',
                    text: 'Top Directors',
                    description: 'Lorem ipsum amet, consectetur adipiscing. Pallentesque ultriecies justo tellus.',

                },
                {
                    image: '/img/service-5.svg',
                    text: 'Minute Editing',
                    description: 'Lorem ipsum amet, consectetur adipiscing. Pallentesque ultriecies justo tellus.',

                },
                {
                    image: '/img/service-6.svg',
                    text: 'Versatile Actors',
                    description: 'Lorem ipsum amet, consectetur adipiscing. Pallentesque ultriecies justo tellus.',

                },



            ],

            works: [
                {
                    image: '/img/work-1.jpg',
                    title: 'Seventeenth Summer',
                    type: 'Commercial, Music Video',

                },
                {
                    image: '/img/work-2.jpg',
                    title: 'A Message To Space',
                    type: 'Short Film',

                },
                {
                    image: '/img/work-3.jpg',
                    title: 'The Most Beatiful Thing',
                    type: 'Music Video',

                },
                {
                    image: '/img/work-4.jpg',
                    title: 'Permission To Speak',
                    type: 'Documentary',

                },
                {
                    image: '/img/work-5.jpg',
                    title: 'Explore our Space',
                    type: 'Film Noir',

                },
                {
                    image: '/img/work-6.jpg',
                    title: 'Film Production',
                    type: 'Blaxploitation',

                },




            ]
        }
    }
}

</script>

<template>

    <main>

        <!-- Section con ITEM SERVICE -->
        <section class="container-services">

            <h4>Pelicula Studio</h4>
            <h2>This is what we do</h2>

            <div class="row-serv">

                <ItemService 
                v-for="currentService in services"
                :TypeService="currentService"
                ></ItemService>

            </div>

            
        </section>

        <!-- SECTION  -->
        <SectionAboutUS></SectionAboutUS>

         <!-- Section con ITEM SERVICE -->
        <section class="container-works">

            <h4>Your Watchlist</h4>
            <h2>Best Hits Movies</h2>

            <div class="row-work">

                <ItemWork 
                v-for="currentWork in works"
                :SingleWork="currentWork"
                ></ItemWork>

            </div>


        </section>

        <!-- SECTION  -->
        <SectionNumbers></SectionNumbers>

        <!-- SECTION  -->
        <SectionTeam></SectionTeam>

        <!-- SECTION  -->
        <SectionQuotes></SectionQuotes>


        <SectionBlog></SectionBlog>

        <!-- SECTION  -->
        <SectionIcons></SectionIcons>

    </main>
    
</template>

<style lang="scss">

main {
    width: 100%;

    .container-services,
    .container-works {

        max-width: 1400px;
        margin: 0 auto;
        padding: 115px 0px;

        h4 {
            text-transform: uppercase;
            text-align: center;
            font-size: 10px;

            padding-bottom: 35px;
        }

        h2 {
            text-transform: uppercase;
            font-size: 30px;
            text-align: center;

            padding-bottom: 65px;

        }

        .row-serv {
            display: flex;
            flex-wrap: wrap;
            gap: 50px 100px;
        }

        .row-work {
            display: flex;
            flex-wrap: wrap;
            gap: 50px 30px;

        }

    }
}

</style>