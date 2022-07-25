<template>
    <footer>
        <div id="footer-top">
            <div class="container">
                <div class="list-column">
                    <h4>{{DcComics.title}}</h4>
                    <ul>
                        <li v-for="link in DcComics.links" :key="link">{{link}}</li>
                    </ul>
                </div>
                <div class="list-column">
                    <h4>{{Shop.title}}</h4>
                    <ul>
                        <li v-for="link in Shop.links" :key="link">{{link}}</li>
                    </ul>
                </div>
                <div class="list-column">
                    <h4>{{DC.title}}</h4>
                    <ul>
                        <li v-for="link in DC.links" :key="link">{{link}}</li>
                    </ul>
                </div>
                <div class="list-column">
                    <h4>{{Sites.title}}</h4>
                    <ul>
                        <li v-for="link in Sites.links" :key="link">{{link}}</li>
                    </ul>
                </div>
                <div>
                    <img id="background-logo" src="../assets/img/dc-logo-bg.png" alt="dc logo">
                </div>
            </div>
        </div>
        <div id="footer-bottom">
            <div class="container">
                <a id="sign-up" src="#">SIGN-UP NOW</a>
                <nav>
                    <a id="follow-us" src="#">FOLLOW US</a>
                    <ul>
                        <li><a href="#"><img src="../assets/img/footer-facebook.png" alt="facebook logo"></a></li>
                        <li><a href="#"><img src="../assets/img/footer-twitter.png" alt="twitter logo"></a></li>
                        <li><a href="#"><img src="../assets/img/footer-youtube.png" alt="youtube logo"></a></li>
                        <li><a href="#"><img src="../assets/img/footer-pinterest.png" alt="pinterest logo"></a></li>
                        <li><a href="#"><img src="../assets/img/footer-periscope.png" alt="periscope logo"></a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'BaseFooter',
    props:{
        DcComics: Object,
        Shop: Object,
        DC: Object,
        Sites: Object,
    }
    }

</script>

<style lang="scss" scoped>
@import '../assets/sass/vars';
/* FOOTER TOP */
    #footer-top {
        background-image: url('../assets/img/footer-bg.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        padding: 2rem 0;
        text-align: center;

        position: relative;

        .container {
        display: flex;
        flex-wrap: wrap;

            .list-column {
            padding-left: 1rem;

                h4{
                    font-size: 1.2rem;
                    padding-bottom: 0.4rem;
                    text-align: start;

                }

                ul {
                padding: 0;
                    li{
                    font-size: 1rem;
                    font-weight: lighter;
                    text-align: start;
                    padding: 0.2rem 0;
                    }
                }
            }
        }
    }

    #background-logo {
        max-height: 350px;

        position: absolute;
        top: 50%;
        right: 5rem;
        transform: translateY(-50%);  
    }

/* FOOTER BOTTOM */
    #footer-bottom {
        height: 100px;
        background-color: #303030;

            .container {
            height: 100%;
            
                #sign-up {
                    padding: 0.5rem;
                    border: 1px solid $color_blue;
                    cursor: pointer;
                    color: #FFF
                    }
            }

            nav {

                #follow-us {
                color: $color_blue
                }

                li {
                margin-left: 1rem;
                }

                img {
                max-width: 1.5rem;
                }
            }
    }
    
    #footer-bottom .container,
    #footer-bottom nav,
    #footer-bottom ul {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
</style>