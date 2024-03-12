<script>
import ItemFooter from '../components/Items/ItemFooter.vue';

export default {
    name: 'AppFooter',

    components: { 

        ItemFooter, 

    },


    data() {
        return {

            // Array contenente elementi per link top footer
            links: [
                {
                    title: 'Information',
                    voices: [
                        'Product Support',
                        'Checkout',
                        'Report Abuse',
                        'Redeem Vaoucher',
                        'Order Stutus',
                    ]

                },
                {
                    title: 'Useful Links',
                    voices: [
                        'Policies & Rules',
                        'Privacy Policy',
                        'License Policy',
                        'My Account',
                        'Locality',
                    ]

                },

            ],


        }
    }
}

</script>

<template>

    <footer>
        <div class="top-footer">

            <div class="list-footer link-footer">

                <div class="list-footer contact-info">
                    <div class="title-footer">Contact Info</div>
                    <div class="info">
                        <img class="location-icon" src="/img/footer-location-dot-solid.svg" alt="location icon">
                        <div>2/45 Tower Street, New York USA</div>
                    </div>
                    <div class="info">
                        <img src="/img/footer-phone-solid.svg" alt="phone icon">
                        <div>Call Us ON 0800 840 1010</div>
                    </div>
                    <div class="info">
                        <img src="/img/footer-envelope-soli.svg" alt="phone icon">
                        <a href="mailto:Demo@Example.com">Demo@Example.com</a>
                    </div>

                </div>
                <ItemFooter 
                    v-for="currentList in links"
                    :Links="currentList"
                ></ItemFooter>
            </div>

            <div class="list-footer form-footer">
                <div class="title-footer">Newsletter</div>
                <span>Subscribe To Receive Inspiration, <br>Ideas & News In Your Inbox.</span>
                <form>
                    <input type="email" placeholder="Enter Your Email">
                    <button>
                        <a href="">Subscribe</a>    
                    </button>
                </form>


            </div>

        </div>

        <div class="bottom-footer">
            <p>&#169; 2023 All Right Reserved. Developed By TempleteMela</p>
        </div>

    </footer>

</template>

<style lang="scss">

@use '../style/variables.scss' as *;

footer {
    width: 100%;
    background-color: $primary_color;

    .top-footer {
        display: flex;
        justify-content: space-between;

        max-width: 1400px;
        margin: 0 auto;

        padding: 115px 0px;

        .list-footer {
            display: flex;
            flex-direction: column;
        }

        .title-footer {
            text-transform: uppercase;
            font-weight: bold;
            color: $secondary_white;
            padding-bottom: 40px;
        }


        .info {
            display: flex;
            justify-content: flex-start;

            width: 200px;
            gap: 20px;
            padding-bottom: 25px;

            img {
                height: 20px;

            }

            div {
                color: #CCCCCC;
                font-size: 14px;
                line-height: 30px;

            }

            a {
                text-decoration: none;
                color: #CCCCCC;
                font-size: 14px;
            }
        }

        .link-footer {
            display: flex;
            flex-direction: row;
            gap: 230px;

            
        }

        .form-footer {

            span {
                padding-bottom: 30px;
                color: #CCCCCC;
                line-height: 30px;
            }

            form {
                display: flex;
                flex-direction: column;
            }
            input {
                width: 280px;
                height: 50px;

                padding: 10px 20px;
                margin-bottom: 15px;

                border: none;
                color: $secondary_color;
                background-color: #1A1A1A;

            }
        }

    }

    .bottom-footer {
        max-width: 1400px;
        margin: 0 auto;
        color: #CCCCCC;
        border-top: 1px solid $secondary_color;

        p {
            text-align: center;

            padding: 20px 0px;
        }
    }

}

</style>