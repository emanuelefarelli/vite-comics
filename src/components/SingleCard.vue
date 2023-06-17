<script>
export default {
    name: 'SingleCard',
    props: {
        cardElement : Object
    },
}
</script>

<template>
    <article>
        <img :src="cardElement.thumb" alt="comic thum image">
        <h2>
            {{ cardElement.series }}
        </h2>
    </article>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variables.scss' as *;
    article{
        width: calc(100% / 6);
        margin-bottom: 3rem;
        padding: 0.5rem;
        img{
            width: 180px;
            height: 180px;
            object-fit: cover;
            object-position: 0 0;
        }
        h2{
            margin-top: 1rem;
            text-transform: uppercase;
            font-size: $fontSizeSmall;
        }
    }
</style>