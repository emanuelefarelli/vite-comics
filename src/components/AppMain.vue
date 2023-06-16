<script>
export default{
    name: 'AppMain',
    data(){

    }
}
</script>


<template>
    <main>
        <div class="container">
            <h1> -- Content goes here -- </h1>
        </div>
    </main>
</template>


<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variables.scss' as *;
    main{
        @include flex(row,start,center);
        background-color: black;
        color: white;
        height: calc(100vh - 7rem - 9rem - 28rem - 7rem);
        div{
            @include marginAuto;
            h1{
                font-size: $fontSizeBig;
            }
        }
    }
</style>