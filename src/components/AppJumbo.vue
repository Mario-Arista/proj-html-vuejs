<script>

export default {
    name: 'AppJumbo',
}

</script>

<template>

    <div class="container">

        <div class="row-jumbo">

            <div class="jumbo">

                <!--  -->
                <h3>Cinema Studio</h3>
                <h1>Action and <br> inspire people</h1>
                <button>
                    <a href="">Read more</a>
                </button>

                <!-- Frecce per funzionamento slider -->
                <div class="slider-arrows">
                    <div class="arrow-left-slider">
                        <img class="arrow" src="/img/icon-left-arrow.svg" alt="left arrow">
                    </div>
                    <div class="arrow-right-slider">
                        <img class="arrow" src="/img/icon-right-arrow.svg" alt="left arrow">
                    </div>
                </div>

            </div>

        </div>

    </div>

    
</template>

<style lang="scss">

@use '../style/variables.scss' as *;



.row-jumbo {
    position: relative;

    display: flex;
    align-items: center;

    height: 800px;
    

    background-image: url('/img/jumbo-3.jpg');
    background-size: cover;


    .jumbo {
        max-width: 1400px;
        padding-left: 250px;
        
        // STILE FRECCE

        .slider-arrows {
            position: absolute;
            left: 0px;
            top: 50%;
            transform: translateY(-50%);

            display: flex;
            justify-content: space-between;
            align-items: center;

            width: 100%;

            padding: 0px 10px;

            .arrow-left-slider, 
            .arrow-right-slider {
                display: flex;
                justify-content: center;
                align-items: center;

                width: 40px;
                height: 40px;
                background-color: rgba(0, 0, 0, 0.584);

                .arrow {
                    width: 10px;
                    filter: invert(1.85);

                }
            }

        }
    }
}





</style>