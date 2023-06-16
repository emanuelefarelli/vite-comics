<script>
export default{
    name: 'AppHeader',
    data(){
        return{
            linkList:[
                {
                title: 'characters',
                link: '#'
                },
                {
                title: 'comics',
                link: '#'
                },
                {
                title: 'movies',
                link: '#'
                },
                {
                title: 'tv',
                link: '#'
                },
                {
                title: 'games',
                link: '#'
                },
                {
                title: 'collectibles',
                link: '#'
                },
                {
                title: 'videos',
                link: '#'
                },
                {
                title: 'fans',
                link: '#'
                },
                {
                title: 'news',
                link: '#'
                },
                {
                title: 'shop',
                link: '#'
                },
            ],
        }
    }
}
</script>


<template>
    <header class="container">
        <img src="../assets/img/dc-logo.png" alt="brand Logo">
        <ul>
            <li v-for="linkObj in linkList">
                <a :href="linkObj.link">
                    {{ linkObj.title }}
                </a>
            </li>
        </ul>
    </header>
</template>


<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variables.scss' as *;

    header{
        @include marginAuto;
        height: 7rem;
        @include flex(row, space-between, center);
        img{
            height: 70%;
        }
        ul{
            @include flex();
            height: 100%;
            li{
                @include flex();
                height: 100%;
                margin-left: 2rem;
                text-transform: uppercase;
                font-weight: 600;
                font-size: $fontSizeSmall;
            }
            li:hover{
                @include flex();
                height: 100%;
                color: $blueColor;
                border-bottom: 3px solid $blueColor;
            }
        }
    }

</style>