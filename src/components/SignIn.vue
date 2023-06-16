<script>
export default{
    name: 'SingIn',
    data(){

    }
}
</script>


<template>
    <section class="sign-in">
        <div class="container">
            <button>
                sign-up now!
            </button>
            <ul>
                <li>
                    <h2>
                        follow us
                    </h2>
                </li>
                <li class="social-link">
                    <img src="../assets/img/footer-facebook.png" alt="social logo">
                </li>
                <li class="social-link">
                    <img src="../assets/img/footer-twitter.png" alt="social logo">
                </li>
                <li class="social-link">
                    <img src="../assets/img/footer-youtube.png" alt="social logo">
                </li>
                <li class="social-link">
                    <img src="../assets/img/footer-pinterest.png" alt="social logo">
                </li>
                <li class="social-link">
                    <img src="../assets/img/footer-periscope.png" alt="social logo">
                </li>
            </ul>
        </div>
    </section>
</template>


<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variables.scss' as *;
    section{
        background-color: #303030;
        height: 7rem;
        div{
            height: 100%;
            @include marginAuto;
            @include flex(row,space-between,center);
            button{
                padding: 0.5rem 1rem;
                border-radius: 0;
                border: 3px solid $blueColor;
                background-color: #303030; 
                color: white;
                text-transform: uppercase;
                font-size: $fontSizeMedium;
            } 

            ul{
                @include flex(row,center,center);
                li{
                    margin-right: 0.5rem;
                    h2{
                        font-size: $fontSizeMedium;
                        text-transform: uppercase;
                        color: $blueColor;
                    }
                }
            }
        }
    }
</style>