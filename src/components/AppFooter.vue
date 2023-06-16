<script>
export default{
    name: 'AppFooter',
    data(){
        return{

            dcComicsList: [
                {
                    title: 'Characters',
                    link: '#'
                },
                {
                    title: 'Comics',
                    link: '#'
                },
                {
                    title: 'Movies',
                    link: '#'
                },
                {
                    title: 'TV',
                    link: '#'
                },
                {
                    title: 'Games',
                    link: '#'
                },
                {
                    title: 'Videos',
                    link: '#'
                },
                {
                    title: 'News',
                    link: '#'
                },
            ],
            shopList: [
                {
                    title: 'Shop DC',
                    link: '#'
                },
                {
                    title: 'Shop Dc Collectibles',
                    link: '#'
                },
            ],
            dcList: [
                {
                    title: 'Terms of use',
                    link: '#'
                },{
                    title: 'Privacy policy(New)',
                    link: '#'
                },{
                    title: 'Ad Choises',
                    link: '#'
                },{
                    title: 'Adversiting',
                    link: '#'
                },{
                    title: 'Jobs',
                    link: '#'
                },{
                    title: 'Subscription',
                    link: '#'
                },{
                    title: 'Talent Workshops',
                    link: '#'
                },{
                    title: 'CPSC Certificates',
                    link: '#'
                },{
                    title: 'Ratings',
                    link: '#'
                },{
                    title: 'Shop Hello',
                    link: '#'
                },{
                    title: 'Contact Us',
                    link: '#'
                },
            ],
            sitesList: [
                {
                    title: 'DC',
                    link: '#'
                },{
                    title: 'MAD Magazine',
                    link: '#'
                },{
                    title: 'DC Kids',
                    link: '#'
                },{
                    title: 'DC Universe',
                    link: '#'
                },{
                    title: 'DC Power Visa',
                    link: '#'
                },
            ],
        }
    }
}   
</script>


<template>
    <footer>
        <section class="container links-list">
            <div class="link-list">
                <ul>
                    <li>
                        <h2>
                            dc comics
                        </h2>
                    </li> 
                    <li v-for="ListObj in dcComicsList">
                        <a :href="ListObj.link">
                            {{ ListObj.title }}
                        </a>
                    </li>
    
                    <li>
                        <h2>
                            shop
                        </h2>
                    </li> 
                    <li v-for="ListObj in shopList">
                        <a :href="ListObj.link">
                            {{ ListObj.title }}
                        </a>
                    </li>
                </ul>
                <ul>
                    <li>
                        <h2>
                            dc
                        </h2>
                    </li> 
                    <li v-for="ListObj in dcList">
                        <a :href="ListObj.link">
                            {{ ListObj.title }}
                        </a>
                    </li>
                </ul>
                <ul>
                    <li>
                        <h2>
                            sites
                        </h2>
                    </li> 
                    <li v-for="ListObj in sitesList">
                        <a :href="ListObj.link">
                            {{ ListObj.title }}
                        </a>
                    </li>
                </ul>
            </div>
            <img src="../assets/img/dc-logo-bg.png" alt="brand logo decoration">
        </section>
    </footer>
</template>


<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variables.scss' as *;

    footer{
        height: 28rem;
        background-image: url('../assets/img/footer-bg.jpg');
        background-size: contain;
        section.links-list{
            height: 100%;
            overflow: hidden;
            @include flex(row,space-between,center);
            @include marginAuto;
            div{
                display: flex;
                align-items: flex-start;
                color: white;
                ul{
                    height: 100%;
                    margin-right: 1.5rem;
                    li{
                        padding-bottom: 0.5rem;
                        h2{
                            text-transform: uppercase;
                            font-size: $fontSizeBig;
                            margin-bottom: 0.8rem;
                        }
    
                        a{
                            font-size: $fontSizeMedium;
                            color: gray;
                        }
                        a:hover{
                            color: white;
                        }
                    }
                }
            }
            img{
                height: 600px;
            }
        }
    }

</style>