<script>

export default {
    name: 'SectionQuotes',

    data() {
        return {

            // Indice della citazione attualmente visualizzata
            currentIndex: 0, 
            
            // Array con elementi per partner
            partnersQuotes: [
                {
                    src: '/img/quote-img-1.jpg',
                    fullName: 'Jasmine Figueroa',
                    job: 'Designer',
                    quote: 'Curabitur bibendum ex ut blandit viverra. Nunc lobortis mi dui, id Etiam tempar sit amet metus in bibendum. Nunc eros risus, pellentesque a augue pellentesque fringilla eget mi eu mollis. Mauris comodo.',
                },
                {
                    src: '/img/quote-img-2.jpg',
                    fullName: 'Sarah Anderson',
                    job: 'Creative',
                    quote: 'Love’s not Time’s fool, though rosy lips and cheeks, Within his bending sickle’s compass come; Love alters not with his brief hours and weeks, But bears it out even to the edge of doom.',
                },
                {
                    src: '/img/quote-img-3.jpg',
                    fullName: 'John Simpson',
                    job: 'Cameraman',
                    quote: 'Curabitur bibendum ex ut blandit viverra. Nunc lobortis mi dui, id Etiam tempar sit amet metus in bibendum. Testo non a caso, perchè sono bello bello in modo assurdo e Derek Zoolander è il mio mito. Una cosa importante da sottolineare.',
                },
            ]
        };
        
    },

    methods: {

        // Metodo per cambiare la citazione alla numero uno
        QuoteNumberOne() {
            this.currentIndex = 0;
        },
        // Metodo per cambiare la citazione alla numero due
        QuoteNumberTwo() {
            this.currentIndex = 1;
        },
        // Metodo per cambiare la citazione alla numero tre
        QuoteNumberThree() {
            this.currentIndex = 2;
        }
    }

}

</script>

<template>

    <section class="container for-height">

        <div class="row-quote parallax">

            <div class="quote">

                <img class="quote-icon" src="/img/quote-icon.svg" alt="icona quote">
                <p>{{ partnersQuotes[currentIndex].quote }}</p>
                <div class="single-partner">
                    <img :src="partnersQuotes[currentIndex].src" :alt="partnersQuotes[currentIndex].name">
                    <div class="info-partner">
                        <div class="name-partner">{{ partnersQuotes[currentIndex].fullName }}</div>
                        <div class="position-partner">{{ partnersQuotes[currentIndex].job }}</div>
                    </div>
                </div>

                <div class="icon-to-change">

                    <i class="fa-solid fa-circle" @click="QuoteNumberOne()"></i>
                    <i class="fa-solid fa-circle" @click="QuoteNumberTwo()"></i>
                    <i class="fa-solid fa-circle" @click="QuoteNumberThree()"></i>

                </div>

            </div>

        </div>

    </section>
    

</template>

<style lang="scss">

@use '../../style/variables.scss' as *;


.row-quote {    
    display: flex;
    align-items: center;
    justify-content: center;

    width: 100%;
    height: 600px;

    background-image: url('/img/quote-background.jpg');
    background-size: cover;
    background-position: center center;


    .quote {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;

        max-width: 40%;
        color: $secondary_white;

        .quote-icon {
            width: 50px;
            filter: invert(1.85);
            padding-bottom: 45px;
        }

        p {
            text-align: center;
            padding-bottom: 30px;
            line-height: 25px;
            letter-spacing: 2px;
            font-family: "Roboto Condensed", sans-serif;

        }

        .single-partner {
            display: flex;
            align-items: center;
            gap: 15px;
            padding-bottom: 30px;

            img {
                width: 60px;
                height: 60px;
                border-radius: 50%;
            }
            .info-partner {

                .name-partner {
                    text-transform: uppercase;
                    font-size: 14px;
                    letter-spacing: 1px;
                    font-weight: bold;
                }

                .position-partner {
                    font-size: 12px;
                    font-family: "Roboto Condensed", sans-serif;

                }

            }

        }
    }


}


.icon-to-change {
    
    display: flex;
    gap: 10px;

    i  {

    font-size: 10px;

    }   

}
</style>