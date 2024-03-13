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

        <!-- TOP FOOTER -->
        <div class="top-footer">

            <div class="total-footer">

                <div class="left-part-footer">

                    <div class="contact-info">
                        <div class="title-footer">Contact Info</div>
                        <div class="info">
                            <div>
                                <img class="location-icon" src="/img/footer-location-dot-solid.svg" alt="location icon">
                            </div>
                            <span>2/45 Tower Street, New York USA</span>
                        </div>
                        <div class="info">
                            <div>
                                <img class="location-icon" src="/img/footer-phone-solid.svg" alt="phone icon">
                            </div>
                            <span>Call Us ON 0800 840 1010</span>
                        </div>
                        <div class="info">
                            <div>
                                <img src="/img/footer-envelope-soli.svg" alt="phone icon">
                            </div>
                            <a href="mailto:Demo@Example.com">Demo@Example.com</a>
                        </div>

                    </div>

                    <div class="item-footer-container">

                        <ItemFooter 
                        v-for="currentList in links"
                        :Links="currentList"
                        ></ItemFooter>

                    </div>

 

                </div>

                <div class="form-footer">

                    <div class="title-footer">Newsletter</div>
                    <div class="text-cta">Subscribe To Receive Inspiration, <br>Ideas & News In Your Inbox.</div>
                    <form>
                        <input type="email" placeholder="Enter Your Email">
                        <button>
                            <a href="">Subscribe</a>    
                        </button>
                    </form>


                </div>
                

            </div>

        </div>


        <!-- Bootom FOOTER -->
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

    // STILE TOP FOOTER 

    .top-footer {
        max-width: 1400px;
        margin: 0 auto;

        padding: 115px 0px;

        .total-footer {
            display: flex;
            justify-content: space-between;

        }

        .left-part-footer {
            display: flex;
            
        }
        .item-footer-container {
            display: flex;
            gap: 230px;
        }

        .contact-info {
            margin-right: 100px;
        }

        .title-footer {
            text-transform: uppercase;
            font-weight: bold;
            color: $secondary_white;
            padding-bottom: 40px;
        }


        .info {
            display: flex;
            align-items: flex-start;

            width: 200px;
            gap: 20px;
            padding-bottom: 25px;

            div {
                height: 20px;
                width: 20px;
                
                img {
                
                    width: 100%;

                    &.location-icon {
                        padding-top: 5px;
                    }
                }
            }
            

            span {
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
            gap: 100px;

            
        }

        .form-footer {

            .text-cta {
                margin-bottom: 25px;
                color: #CCCCCC;
                line-height: 30px;
                font-size: 14px;

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


    // STILE BOTTOM FOOTER 
    .bottom-footer {
        max-width: 1400px;
        margin: 0 auto;
        color: #CCCCCC;
        border-top: 1px solid #333333;

        p {
            text-align: center;

            padding: 20px 0px;
        }
    }

}

</style>