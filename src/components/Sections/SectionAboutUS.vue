<script>

export default {
    name: 'SectionAboutUS',

}

</script>

<template>

    <section class="container-fluid">

        <div class="row-about">

            <div class="about">

                <h4>About us</h4>
                <h2>High quality Cinematics</h2>
                <p>Orci varius penatibus et magnis dis parturient in the montes, nascetur ridiculus mus. Nulla a nisi ut mi efficitur hendrerit. Nunc hurna. Quisque a partr hendrerit purus erat, nec dapibus sem sed. Phasellus sed eli molestie, parttitor ligula of the egestas, mattiis augue. Quisque et rhoncus justo. Suspendisse luctus pharetra eleme tcondimentus</p>
                <button>
                    <a href="">Read more</a>
                </button>

            </div>

        </div>

    </section>
    

</template>

<style lang="scss" scoped>

@use '../../style/variables.scss' as *;

.row-about {

    display: flex;
    align-items: center;
    justify-content: flex-end;

    height: 570px;

    padding-right: 225px;

    background-image: url('/img/About-Us.jpg');
    background-size: contain;

    .about {
        max-width: 730px;
        color: $primary_white;

        h4 {
            padding-bottom: 30px;
            font-size: 12px;
            text-transform: uppercase;
        }

        h2 {
            padding-bottom: 50px;
            font-size: 30px;
            text-transform: uppercase;
        }

        p {
            padding-bottom: 50px;
            line-height: 25px;
        }
    }
}

</style>