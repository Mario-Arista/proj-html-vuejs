<script>

export default {
    name: 'SectionTeam',

}

</script>

<template>

    <section class="container">

        <div class="row-team">

            <h4>The Pericuros</h4>
            <h2>Meet The team</h2>

            <div class="team">

                <div class="single-member">
                    <img src="/img/Team-1.jpg" alt="Foto di Fabrizio Guerra, Main Director di CINEMATO">
                    <div class="name-team-member">Fabricio Guerra</div>
                    <div class="position-team-member">Main Director</div>
                </div>

                <div class="single-member">
                    <img src="/img/Team-2.jpg" alt="Foto di Umberto Pagoda, Main Writer di CINEMATO">
                    <div class="name-team-member">Umberto Pagoda</div>
                    <div class="position-team-member">Main Writer</div>
                </div>

                <div class="single-member">
                    <img src="/img/Team-3.jpg" alt="Foto di Gloria Ricasso, Main Producer di CINEMATO">
                    <div class="name-team-member">Gloria Ricasso</div>
                    <div class="position-team-member">Main Producer</div>
                </div>

                <div class="single-member">
                    <img src="/img/Team-4.jpg" alt="Foto Lio Napoin, Cameraman di CINEMATO">
                    <div class="name-team-member">Lio Napoin</div>
                    <div class="position-team-member">Cameraman</div>
                </div>

            </div>

        </div>

    </section>

</template>

<style lang="scss">

@use '../../style/variables.scss' as *;

.row-team {
   margin: 0 auto;

   padding: 115px 0px;

    max-width: 1400px;
    background-color: $primary_white;
    color: $primary_color;

    h4 {

        text-align: center;
        padding-bottom: 25px;
    }

    h2 {
        text-align: center;
        padding-bottom: 40px;
    }

    .team {
        display: flex;
        align-items: center;
        gap: 30px;

        .single-member {
            display: flex;
            flex-direction: column;
            justify-content: flex-start;

            width: calc(100% / 4 - 30px / 4 * 3);

            img {
                width: 100%;
                display: block;

                padding-bottom: 20px;
            }

            .name-team-member {
                text-transform: uppercase;
                font-weight: bold;
                text-align: center;
                font-size: 14px;
                letter-spacing: 2px;
                
                padding-bottom: 15px;
            }
            .position-team-member {
                text-align: center;
                font-size: 12px;
                font-family: "Roboto Condensed", sans-serif;
                letter-spacing: 1px;
                color: $secondary_color;
            }

        }



    }

}

</style>