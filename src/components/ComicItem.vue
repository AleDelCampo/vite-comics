<script>
export default {
    name: 'ComicItem',
 
    props: {
        
        comicTitle: String,
        comicPoster: String
    },
    
    data() {
    },
}
</script>

<template>
    
    <div>
        <img :src="comicPoster" :alt="comicTitle">
        <h4>{{ comicTitle }}</h4>
    </div>
    
</template>

<style lang="scss">

</style>