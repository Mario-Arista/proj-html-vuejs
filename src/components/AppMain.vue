<script>
import ItemService from './Items/ItemService.vue';
import SectionAboutUS from './Sections/SectionAboutUS.vue';
import SectionWorks from './Sections/SectionWorks.vue';
import SectionNumbers from './Sections/SectionNumbers.vue';
import SectionTeam from './Sections/SectionTeam.vue';
import SectionQuotes from './Sections/SectionQuotes.vue';
import SectionBlog from './Sections/SectionBlog.vue';
import SectionIcons from './Sections/SectionIcons.vue';


export default {
    name: 'AppMain',

    components: { 
        ItemService,  
        SectionAboutUS, 
        SectionWorks, 
        SectionNumbers,
        SectionTeam,
        SectionQuotes,
        SectionBlog,
        SectionIcons,
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



            ]
        }
    }
}

</script>

<template>

    <main>

        <!-- Section con ITEM SERVICE -->
        <section class="container-services">

            <h5>Pelicula Studio</h5>
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

        <SectionWorks></SectionWorks>
        <SectionNumbers></SectionNumbers>
        <SectionTeam></SectionTeam>
        <SectionQuotes></SectionQuotes>
        <SectionBlog></SectionBlog>
        <SectionIcons></SectionIcons>

    </main>
    
</template>

<style lang="scss">

main {
    width: 100%;

    .container-services {

        max-width: 1200px;
        margin: 0 auto;
        padding: 115px 0px;

        h5 {
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

    }
}

</style>