<script>

export default {
    name: 'SectionQuotes',

}

</script>

<template>

    <section class="container for-height">

        <div class="row-quote">

            <div class="quote">

                <img class="quote-icon" src="/img/quote-icon.svg" alt="icona quote">
                <p>Curabitur bibendum ex ut blandit viverra. Nunc lobortis mi dui, id Etiam tempar sit amet metus in bibendum. Nunc eros risus, pellentesque a augue pellentesque fringilla eget mi eu mollis. Mauris comodo.</p>
                <div class="single-partner">
                    <img src="/img/quote-img-1.jpg" alt="Foto di Jasmine Figueroa">
                    <div class="info-partner">
                        <div class="name-partner">Jasmine Figueroa</div>
                        <div class="position-partner">Designer</div>
                    </div>

                </div>
                <div class="icon-to-change">
                        <img src="/img/icon-hamburger.svg" alt="">
                        <img src="/img/icon-hamburger.svg" alt="">
                        <img src="/img/icon-hamburger.svg" alt="">
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

    // Stile non come da progetto, ma mi da troppo fastidio vederlo in quel modo
    background-image: url('/img/quote-background.jpg');
    background-size: cover;
    background-position: center center;

    // Stile come da file commentato
    // background-position-y: 250px;
    // background-position-x: 0px;

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

            .icon-to-change {
                
                img {
                    filter: invert(1.85);
                }
                    
            }
        }
    }


}
</style>