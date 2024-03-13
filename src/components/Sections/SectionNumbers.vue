<script>

export default {
    name: 'SectionNumbers',

}

</script>

<template>

    <section class="container">

        <div class="row-numbers">

            <div id="numbers">

                <div class="number-el">
                    <div class="result">150</div>
                    <div class="text-number">satisfied Clients</div>
                </div>

                <div class="number-el">
                    <div class="result">3+</div>
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

    background-image: url('/img/section-numbers-background.jpg');
    background-size: cover;
    background-position-y: 500px;

    #numbers {
        display: flex;
        gap: 200px;

        max-width: 1400px;

        color: $primary_white;

        .number-el {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 20px;

            width: calc(100% / 4 - 200px / 4 * 3);

            .result {
                
                font-size: 40px;
                font-weight: bold;
            }

            .text-number {
                font-size: 14px;
                font-weight: bold;

                text-transform: uppercase;
                align-items: center;
                white-space: nowrap;
            }

        }
    }

}

</style>