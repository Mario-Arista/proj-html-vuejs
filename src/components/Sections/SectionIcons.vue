<script>

export default {
    name: 'SectionIcons',

}

</script>

<template>

    <section class="container">

        <div class="row-icons">

            <div id="icons">

                <img src="/img/section-icons-1.png" alt="icona uno">
                <img src="/img/section-icons-2.png" alt="icona uno">

                <img src="/img/section-icons-3.png" alt="icona uno">

                <img src="/img/section-icons-4.png" alt="icona uno">

                <img src="/img/section-icons-5.png" alt="icona uno">


            </div>

        </div>

    </section>

</template>

<style lang="scss">

@use '../../style/variables.scss' as *;

.row-icons {

    display: flex;
    align-items: center;
    justify-content: center;

    height: 320px;

    background-image: url('/img/section-icons-background.jpg');
    background-size: cover;
    background-position: center;

    #icons {
        display: flex;
        gap: 150px;

        max-width: 1400px;
        padding-left: 30px;
        padding-right: 30px;


        img {
            max-width: 140px;
        }

    }

}

</style>