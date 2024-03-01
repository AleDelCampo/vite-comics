<script>

    export default {
    name: 'AppFooter',

    data() {
        return {
            links: [
                {
                    title: "DC COMICS",
                    list: [
                        'Characters',
                        'Comics',
                        'Movies',
                        'Tv',
                        'Games',
                        'Videos',
                        'News'
                    ]
                },
                {
                    title: "SHOP",
                    list: [
                        'Shop DC',
                        'Shop DC Collectibles',
                    ]
                },{
                    title: "DC",
                    list: [
                        'Terms Of Use',
                        'Privacy policy',
                        'Ad Choices',
                        'Advertising',
                        'Jobs',
                        'Subscriptions',
                        'Talent Workshops',
                        'CPSC Certificates',
                        'Ratings',
                        'Shop Help',
                        'Contact Us'
                    ]
                },{
                    title: "SITES",
                    list: [
                        'DC',
                        'MAD Magazine',
                        'DC Kids',
                        'DC Universe',
                        'DC Power Visa'
                    ]
                }
            ]
        }
    }
}

</script>

<template>
<footer>
    <div id="links-cnt">
    <div id="footer-list" class="list-link pointer">
        <div v-for="linkList in links" class="links-list">
            <h3>{{ linkList.title }}</h3>
            <ul>
                <li v-for="currentLink in linkList.list">
                    {{ currentLink }}
                </li>
            </ul>
        </div>
    </div>
    </div>

    <div id="img-cnt">
        <img src="C:\VITE\vite-comics\src\assets\dc-logo-bg.png" alt="LOGO">
    </div>

</footer>
</template>

<style lang="scss">

#footer-list {
    display: flex;
    justify-content: center;
    gap: 40px
}

#img-cnt {
    width: 400px;
    height: 400px;
    position: relative;
    bottom: -10px;  
    overflow: hidden;
    img {
        width: 100%;
        height: 100%;
    }
}

#links-cnt {
    display: flex;
    flex-direction: column;
}

footer {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    gap: 60px;
    position: relative;
    bottom: 19px;
    overflow: hidden; 
    .list-link {
        
        h3 {
            margin-bottom: 16px;
        }

        ul {
            list-style-type: none;
            font-size: 0.8em;
            color: #959595;
        }
    }
}

.links-list:nth-child(2) {
   position: absolute;
   bottom: 48px;
   left: 358px;
}

</style>