<script>

export default {
    name: 'AppForm',
}

</script>

<template>

    <div class="container-fluid">

        <div class="row-work-with-us">

            <div class="with-us-text">

                <h3>Collaborate</h3>
                <h2>Want to work with us? <br>leave us a message!</h2>
                <p>Duis sit amet congue ipsum. Nulla maximus My venenatis posuere. To the Mauris ut tempus Suspendisse porta tincidunt lectus non of me pellentesque. At A Sed blandit at diam sit amet Orci varius natosque penatibus et dis dis to parturient montes, My Car nascetur ridiculus Sed lacus in erat egestas, quis eleifend lacus imperdiet.</p>

            </div>

            <form>
                <div class="input-merger">
                    <input class="right-input" type="text" name="YourNameame" placeholder="Your Name">
                    <input type="email" name="YourEmail" placeholder="Your Email">
                </div>
                <div class="input-merger">
                    <input class="right-input" type="number" name="YourPhone" placeholder="Mobile Number">
                    <input type="number" name="YourPin" placeholder="Pin Code">
                </div>

                <textarea name="message" rows="6" cols="50">Enter Your Message</textarea>

                <button>
                    <a href="">submit</a>
                </button>
            </form>


        </div>

    </div>

    
</template>

<style lang="scss">

@use '../style/variables.scss' as *;


.row-work-with-us {
    display: flex;
    gap: 50px;

    margin: 0 auto;
    max-width: 1400px;

    padding: 115px 0px;

    .with-us-text {
        width: 50%;

        h3 {
            text-transform: uppercase;
            font-size: 14px;
            color: $primary_color;
            padding-bottom: 30px;
        }

        h2 {
            text-transform: uppercase;
            font-size: 30px;
            color: $primary_color;
            padding-bottom: 30px;

        }

        p {
            text-align: justify;
            font-size: 14px;
            line-height: 30px;
            color: $secondary_color;
        }
    }

    form {
        width: 50%;

        .input-merger {
            padding-bottom: 40px;
            width: 100%;

        }

        input {
            height: 45px;
            width: calc(100% / 2 - 12.5px);
            
            padding-left: 15px;

            border: none;
            border-radius: 8px;
            background-color: $secondary_white;
            color: $secondary_color;

            &.right-input {
                margin-right: 25px;
            }
        }

        textarea {
            width: 100%;
            border: none;

            padding: 15px;


            border-radius: 8px;
            background-color: $secondary_white;
            color: $secondary_color;
        }

        button {
            
            background-color: $primary_color;
            width: 100%;

            margin-top: 25px;

            a {
                color: $primary_white;
            }
        }
        
    }
}

</style>