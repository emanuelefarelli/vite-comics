<script>
import SingleCard from './SingleCard.vue';

export default{
    name: 'AppMain',
    components: {
        SingleCard
    },
    data(){
        return{    
            cardList: [
              {
                  thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                  price: "$19.99",
                  series: "Action Comics",
                  type: "comic book",
              },
              {
                  thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                  price: "$3.99",
                  series: "American Vampire 1976",
                  type: "comic book",
              },
              {
                  thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                  price: "$16.99",
                  series: "Aquaman",
                  type: "graphic novel",
              },
              {
                  thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                  price: "$2.99",
                  series: "Batgirl",
                  type: "comic book",
              },
              {
                  thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                  price: "$3.99",
                  series: "Batman",
                  type: "comic book",
              },
              {
                  thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                  price: "$2.99",
                  series: "Batman Beyond",
                  type: "comic book",
              },
              {
                  thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                  price: "$3.99",
                  series: "Batman/Superman",
                  type: "comic book",
              },
              {
                  thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                  price: "$4.99",
                  series: "Batman/Superman Annual",
                  type: "comic book",
              },
              {
                  thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                  price: "$5.99",
                  series: "Batman: The Joker War Zone",
                  type: "comic book",
              },
              {
                  thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                  price: "$6.99",
                  series: "Batman: Three Jokers",
                  type: "comic book",
              },
              {
                  thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                  price: "$4.99",
                  series: "Batman: White Knight Presents: Harley Quinn",
                  type: "comic book",
              },
              {
                  thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                  price: "$16.99",
                  series: "Catwoman",
                  type: "graphic novel",
              },
            ]
        }      
    }    
}

</script>


<template>
    <main>
        <div class="container">
            <SingleCard v-for="cardObj in cardList"
                :cardElement = "cardObj"
            />
            <button>
                Load More
            </button>
        </div>
    </main>
</template>


<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variables.scss' as *;
    main{
        @include flex(row,start,center);
        background-color: #1c1c1c;
        color: white;
        height: 75vh;
        div{
            @include marginAuto;
            display: flex;
            flex-wrap: wrap;
            button{
                @include marginAuto;
                padding: 0.7rem 2.2rem;
                background-color: $blueColor;
                border-radius: 0;
                border: 0px;
                color: white;
                text-transform: uppercase;
                font-size: $fontSizeMedium;
                font-weight: 500;
            }
            button:hover{
                background-color: #1663ac;
            }
        }
    }
</style>