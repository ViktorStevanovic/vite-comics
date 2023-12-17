<template>
    <article>
        <img :src="thumb" alt="">
        <p>{{ series }}</p>
    </article>
</template>
<script>

export default {
    name: 'ComicCard',
    props: {
        series : String,
        price : Number,
        thumb : String,
        type : String,
    }
}   

</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
article{
    width: calc((100% - 5rem) / 6);
    img{
        width: 100%;
        height: 250px;
        object-fit: cover;
        object-position: top;
    }
    p{
        text-transform: uppercase;
        color: $bg-white;
        padding: .75rem 0;
    }
}
    
</style>