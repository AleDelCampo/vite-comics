<script>
export default {
    name: 'AppFeatures',

    data() {
        return {
            icons: [
                {
                    icon: 'src/assets/buy-comics-digital-comics.png',
                    caption: "DIGITAL COMICS",
                },{
                    icon: 'src/assets/buy-comics-merchandise.png',
                    caption: "DC MERCHANDISE",
                },{
                    icon: 'src/assets/buy-comics-subscriptions.png',
                    caption: "SUBSCRIPTION",
                },{
                    icon: 'src/assets/buy-comics-shop-locator.png',
                    caption: "COMIC SHOP LOCATOR",
                },{
                    icon: 'src/assets/buy-dc-power-visa.svg',
                    caption: "DC POWER VISA",
                }
            ]
        }
    }
}
</script>


<template>
    <div id="app-features">
        <div id="dynamic-icons" class="pointer" v-for="icon in icons">
            <img id="img-size" :src="icon.icon">
            <p>{{ icon.caption }}</p>
        </div>
    </div>
</template>


<style lang="scss">

#app-features {
    height: 160px;
    width: 100%;
    background-color: #0282f9;
    justify-content: space-evenly;
    display: flex;
    flex-wrap: wrap;
    padding-left: 380px;
    padding-right: 380px;

    #img-size {
        height: 60px;
       
    }
}

#dynamic-icons:nth-child(5) {
    img {
        height: 100%;
        width: 60px;
    }
}

#dynamic-icons {
    display: flex;
    align-items: center;
    gap: 20px;
}

p {
    font-size: 0.8em;
}
</style>