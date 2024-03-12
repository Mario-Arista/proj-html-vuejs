<script>

export default {
    name: 'SectionNumbers',

}

</script>

<template>

    <section class="container-fluid">

        <div class="row-numbers">

            <div class="numbers">

                <div class="number-el">
                    <div class="result">150</div>
                    <div class="text-number">satisfied Clients</div>
                </div>

                <div class="number-el">
                    <div class="result">3 +</div>
                    <div class="text-number">Our Projects</div>
                </div>

                <div class="number-el">
                    <div class="result">1,906</div>
                    <div class="text-number">Cup of Coffee</div>
                </div>

                <div class="number-el">
                    <div class="result">2</div>
                    <div class="text-number">Our awards</div>
                </div>

            </div>

        </div>

    </section>

</template>

<style lang="scss">

@use '../../style/variables.scss' as *;

.row-numbers {

    display: flex;
    align-items: center;
    justify-content: center;

    height: 310px;

    background-image: url('../../../public/img/section-numbers-background.jpg');
    background-size: cover;
    background-position-y: 500px;

    .numbers {
        display: flex;
        max-width: 1200px;
        gap: 220px;

        color: $primary_white;

        .number-el {
            width: calc(100% / 4 - 220px / 4 * 3)

        }
    }

}

</style>