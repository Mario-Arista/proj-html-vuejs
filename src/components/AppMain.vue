<script>
import SectionServices from './Sections/SectionServices.vue';
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
        SectionServices,  
        SectionAboutUS, 
        SectionWorks, 
        SectionNumbers,
        SectionTeam,
        SectionQuotes,
        SectionBlog,
        SectionIcons,
    },
}

</script>

<template>

    <main>

        <SectionServices></SectionServices>
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
}

</style>