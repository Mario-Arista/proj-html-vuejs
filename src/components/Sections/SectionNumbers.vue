<script>

export default {
    name: 'SectionNumbers',

    data() {
        return {

            // Contatore clienti soddisfatti, parte da 0
            satisfiedClients: 0,
            // Valore massimo per i clienti soddisfatti
            maxSatisfiedClients: 150, 

            // Contatore caffè, parte da 0
            cupsOfCoffee: 0,
            // Valore massimo per le tazze di caffè
            maxCupsOfCoffee: 1906, 

        };
    },

    mounted() {
        this.startCounting();
    },

    methods: {
        startCounting() {
            setInterval(() => {

                if (this.satisfiedClients < this.maxSatisfiedClients) {
                    this.satisfiedClients++;
                }

                if (this.cupsOfCoffee < this.maxCupsOfCoffee) {
                    this.cupsOfCoffee++;
                }

                // Verifico se i valori massimi sono stati raggiunti
                if (this.satisfiedClients === this.maxSatisfiedClients &&
                    this.cupsOfCoffee === this.maxCupsOfCoffee) {
                        
                    // se si interrompo l'intervallo
                    clearInterval(interval);
                }


            }, 100);
        }
    }
}

</script>

<template>

    <section class="container">

        <div class="row-numbers">

            <div id="numbers">

                <div class="number-el">
                    <div class="result">{{ satisfiedClients }}</div>
                    <div class="text-number">Satisfied Clients</div>
                </div>

                <div class="number-el">
                    <div class="result">3+</div>
                    <div class="text-number">Our Projects</div>
                </div>

                <div class="number-el">
                    <div class="result">{{ cupsOfCoffee }}</div>
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