<template lang="">
    <main>
        <section class='upper-main'>
            <div class="hero-section">
                        <img src="../assets/img/jumbotron.jpg" alt="Teen Titans image ">
                    </div>
            <div class="wrapper">
                <section>
                    <ComicCard v-for='book in seriesList'
                    :series = 'book.series'
                    :price = 'book.price'
                    :thumb = book.thumb
                    :type = 'book.type'
                    />          
                </section>
                <button>Load More</button>
            </div>
        </section>
        <!-- Blue lower-main section -->
        <section class='lower-main'>
            <div class="wrapper">
                <section class='shop-icons'>
                    <div>
                        <img src="../assets/img/buy-comics-digital-comics.png" alt="Digital comics icon">
                        <p>Dc comics</p>                   
                    </div>
                    <div>
                        <img src="../assets/img/buy-comics-merchandise.png" alt="Merchandise comics icon">
                        <p>Dc merchandise</p>                   
                    </div>
                    <div>
                        <img src="../assets/img/buy-comics-shop-locator.png" alt="Shop locator icon">
                        <p>Comic shop location</p>                   
                    </div>
                    <div>
                        <img src="../assets/img/buy-comics-subscriptions.png" alt="Subscription comics icon">
                        <p>Subscription</p>                   
                    </div>
                    <div>
                        <img src="../assets/img/buy-dc-power-visa.svg" alt="Dc power visa icon">
                        <p>Dc power visa</p>                   
                    </div>
                </section>
            </div>          
        </section>
        
    </main>
</template>
<script>
import ComicCard from './ComicCard.vue'
export default {
    name: 'AppMain',
    components:{
        ComicCard
    },
    data() {
        return {
            seriesList: [
                {

                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",

                    "price": "$19.99",

                    "series": "Action Comics",

                    "type": "comic book",

                },

                {

                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",

                    "price": "$3.99",

                    "series": "American Vampire 1976",

                    "type": "comic book",

                },

                {

                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",

                    "price": "$16.99",

                    "series": "Aquaman",

                    "type": "graphic novel",

                },

                {

                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",

                    "price": "$2.99",

                    "series": "Batgirl",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",

                    "price": "$3.99",

                    "series": "Batman",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",

                    "price": "$2.99",

                    "series": "Batman Beyond",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",

                    "price": "$3.99",

                    "series": "Batman/Superman",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",

                    "price": "$4.99",

                    "series": "Batman/Superman Annual",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",

                    "price": "$5.99",

                    "series": "Batman: The Joker War Zone",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",

                    "price": "$6.99",

                    "series": "Batman: Three Jokers",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",

                    "price": "$4.99",

                    "series": "Batman: White Knight Presents: Harley Quinn",

                    "type": "comic book",

                },

                {

                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",

                    "price": "$16.99",

                    "series": "Catwoman",

                    "type": "graphic novel",

                },

]
        }
    },
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
main{
    width: 100%;
    .upper-main{
        background-color: $bg-gray;
        .hero-section{
            width: 100%;
            img{
                width: 100%;
                height: 500px;
                object-fit: cover;
                object-position:top;
            }
        }
        .wrapper{
            @include flex(column, space-between,start);
            section{
                @include flex(row, space-between,start);
                flex-wrap: wrap;
                gap: 1rem;
                padding: 2rem 0;
            }
            button{
                align-self: center;
                border: none;
                background-color: $color-blue;
                text-transform: uppercase;
                padding: .75rem 3rem;
                margin-bottom: 1.25rem;
                font-weight: bold;
                color: $bg-white;
            }
        }
    }
    .lower-main{
        background-color: $color-blue;
    }
    .wrapper{
        // width: 100%;
        section{
            margin: 0 auto;
    
            h1{
                color: white;
                padding: 3rem 0;
                font-size: 2rem;
            }
        }
        .shop-icons{
            width: 100%;
            @include flex(row, space-between, center);

            div{
                @include flex(row, space-between, center);
                padding: 2rem 0;
                gap: 1rem;
                color: $bg-white;
                p{
                    text-transform: uppercase;
                }
                img{
                    height: 50px;
                }
            }
            
        }
    }
}   
</style>