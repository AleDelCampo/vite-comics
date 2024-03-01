<script>
export default {
    name: 'ComicItem',
 
    props: {
        
        comicTitle: String,
        comicPoster: String
    },
}
</script>

<template>
    
    <div class="comic">
        <img class="pointer" :src="comicPoster" :alt="comicTitle">
        <h5>{{ comicTitle }}</h5>
    </div>
    
</template>

<style lang="scss">

.comic {
    
    width: calc(100% / 6);
    
    text-align: justify;
    img {
        width: 190px;
        height: 220px;
        margin-bottom: 8px;
    }

    h5 {
        margin-bottom: 40px;
        text-transform: uppercase;
        font-size: 0.8em;
        width: 190px;
    }
}

</style>