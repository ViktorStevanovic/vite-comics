<template lang="">
    <footer>
        <section class="upper-footer">
            <div class="wrapper">
                <section class="footer-nav">
                    <div class="left">
                        <h2>Dc Comics</h2>
                        <ul>
                            <li>Characters</li>
                            <li>Comics</li>
                            <li>Movies</li>
                            <li>TV</li>
                            <li>Games</li>
                            <li>Videos</li>
                            <li>News</li>
                        </ul>
                        <h2>Shop</h2>
                        <ul>
                            <li>Shop DC</li>
                            <li>Shop DC Collectibles</li>
                        </ul>
                    </div>
                    <div class="center">
                        <h2>Dc</h2>
                        <ul>
                            <li>Terms of use</li>
                            <li>Privacy policy (New)</li>
                            <li>Ad Choices</li>
                            <li>Advertising</li>
                            <li>Jobs</li>
                            <li>Subscriptions</li>
                            <li>Talent Workshops</li>
                            <li>CPSC Certificates</li>
                            <li>Ratings</li>
                            <li>Shop Help</li>
                            <li>Contact Us</li>
                        </ul>
                    </div>
                    <div class="right">
                        <h2>Sites</h2>
                        <ul>
                            <li>DC</li>
                            <li>MAD Magazine</li>
                            <li>DC Kids</li>
                            <li>DC Universe</li>
                            <li>DC Power Visa</li>
                        </ul>
                    </div>
                </section>
                <section class="footer-logo">
                    <!-- <img src="../assets/img/dc-logo-bg.png" alt="Big DC logo footer"> -->
                </section>
            </div>
        </section>
        <section class="lower-footer">
            <div class="wrapper">
                <section class='sign-up'>
                    <button>Sign-up now!</button>
                </section>
                <section class="socials">
                    <h3>Follow us</h3>
                    <img src="../assets/img/footer-facebook.png" alt="facebook logo">
                    <img src="../assets/img/footer-twitter.png" alt="twitter logo">
                    <img src="../assets/img/footer-youtube.png" alt="youtube logo">
                    <img src="../assets/img/footer-pinterest.png" alt="pinterest logo">
                    <img src="../assets/img/footer-periscope.png" alt="periscope logo">
                </section>
            </div>
        </section>
    </footer>
</template>
<script>
export default {
    data() {
        return {
            
        }
    },
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

footer{
    width: 100%;
    .upper-footer{
        width: 100%;
        background-image: url('../assets/img/footer-bg.jpg');
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        color: $bg-white;
        .wrapper{
            @include flex(row, space-between, center);
            padding: 2rem 0;
        }
        .footer-nav{
            @include flex(row, center, start);
            gap: 2.5rem;
            h2{
                margin-bottom: .75rem;
                text-transform: uppercase;
                font-size: 1.25rem;
            }
            li{
                color:gray;
                margin-bottom: .25rem;

            }
            
        }
        // .footer-logo{
        //     // background-image: url('../assets/img/dc-logo-bg.png');
        //     // width: 500px;
        //     // height: 100%;
        // }
    }
    .lower-footer{
        background-color: $bg-gray;
        width: 100%;
        .wrapper{
            @include flex(row, space-between, center);
            padding: 2rem 0;
            .sign-up{
                button{
                    border: 1px solid $color-blue;
                    background-color: transparent;
                    color: $bg-white;
                    padding: .75rem 1rem;
                    text-transform: uppercase
                }
            }
            .socials{
                @include flex(row, space-between, center);
                gap: 1rem;
                h3{
                    color: $color-blue;
                    text-transform: uppercase;
                }
            }
        }
    }
    
}

    
</style>