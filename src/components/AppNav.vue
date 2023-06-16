<script>
export default{
    name: 'AppNav',
    data(){
        return{
            navLinkList: [
                {
                    imgSrc: 'buy-comics-digital-comics.png',
                    title: 'digital comics',
                },
                {
                    imgSrc: 'buy-comics-merchandise.png',
                    title: 'dc merchandise',
                },
                {
                    imgSrc: 'buy-comics-subscriptions.png',
                    title: 'subsciption',
                },
                {
                    imgSrc: 'buy-comics-shop-locator.png',
                    title: 'comic shop locator',
                },
                {
                    imgSrc: 'buy-dc-power-visa.svg',
                    title: ' dc power visa',
                },
            ]
        }
    },

    methods:{
        getImagePath: function(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>


<template>
    <nav>
        <ul class="container">
             <li v-for="shopObj in navLinkList">
                <img :src="getImagePath(shopObj.imgSrc)" alt="Item shop image">
                <h2>
                    {{ shopObj.title }}
                </h2>
             </li>
        </ul>
    </nav>
</template>


<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variables.scss' as *;
    nav{
        height: 9rem;
        background-color: $blueColor;
        color: white;
        ul{
            height: 100%;
            @include marginAuto();
            @include flex(row,space-around,center);
            li{
                @include flex;
                img{
                    height: 50px;
                    margin-right: 1rem;
                }
                h2{
                    text-transform: uppercase;
                    font-size: $fontSizeSmall;
                }
            }
        }
    }
</style>