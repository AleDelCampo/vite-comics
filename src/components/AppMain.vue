<script>
import AppFeatures from './AppFeatures.vue';
import AppFooter from './AppFooter.vue';

export default {
    name: 'AppMain',
    name: 'AppFooter',
    components: {
    AppFeatures,
    AppFooter
    },
    name: 'AppMain',
    data() {
        return {
            links: [
                {
                    list: [
                        'CHARACTERS',
                        'COMICS',
                        'MOVIES',
                        'TV',
                        'GAMES',
                        'COLLECTIBLES',
                        'VIDEOS',
                        'FANS',
                        'NEWS',
                        'SHOP',
                    ]
                }
            ]
        }
    }
}



</script>

<template>

  <div id="navbar" class="bar my-display">
  
    <div class="my-display">
        <img src="C:\VITE\vite-comics\src\assets\dc-logo.png" alt="">
    </div>

    
    <div class="text">
        <div v-for="linkList in links">
            <ul id="nav-list">
                <li class="links pointer" v-for="currentLink in linkList.list">
                    {{ currentLink }}
                </li>
            </ul>
        </div>
    </div>
    
  </div>

  <div id="empty-bar" class="my-display">

    <div id="jumbo">
        <img src="C:\VITE\vite-comics\src\assets\jumbotron.jpg" alt="">
    </div>

    
        
  </div>

  <AppFeatures></AppFeatures>

  <div id="footer-cnt">

    <AppFooter></AppFooter>

  </div>

  <div id="socials-footer" class="my-display">

    <div>
        <button class="btn pointer">
            SIGN-UP NOW!
        </button>
    </div>

    <div class="my-display icons-cnt">

        <span class="pointer">
            FOLLOW US
        </span>

        <div class="my-display icons-cnt">
           <img class="pointer" src="C:\VITE\vite-comics\src\assets\footer-facebook.png" alt="Facebook">
           <img class="pointer" src="C:\VITE\vite-comics\src\assets\footer-twitter.png" alt="X">
           <img class="pointer" src="C:\VITE\vite-comics\src\assets\footer-youtube.png" alt="Youtube">
           <img class="pointer" src="C:\VITE\vite-comics\src\assets\footer-pinterest.png" alt="Pinterest">
           <img class="pointer" src="C:\VITE\vite-comics\src\assets\footer-periscope.png" alt="Periscope">
        </div>

    </div>

  </div>

</template>

<style>

/*Regole da creare successivamente come variabili SaSS
perchè molto riusabili.*/
.bar {
    width: 100%;
    height: 130px;
}

.my-display {
    display: flex;
    align-items: center;
    z-index: 99;
}

.text {
    color: black;
}

.links {
    list-style: none;
    border-bottom: 8px solid transparent;
    margin-top: 49px;
    padding-bottom: 49px;
    font-size: 0.9em;
    &:hover {
        color: #0282f9;
        border-bottom: 8px solid #0282f9;
    }
}

.btn {
    background-color: transparent;
    padding: 16px;
    border: 1px solid #0282f9; 
}

/*Regole normali.*/

.pointer {
    cursor: pointer;
}

#jumbo {
    width: 100%;
    height: 400px;
    img {
        height: 100%;
        width: 100%;
        object-fit: cover;
        object-position: top;
    }
}

#navbar {
    background-color: white;
    font-weight: bold;
    justify-content: space-evenly;
}

#nav-list {
    display: flex;
    gap: 20px;
}

#empty-bar {
    font-weight: bold;
    width: 100%;
    justify-content: center;
}

#footer-cnt {
    width: 100%;
    height: 381px;
    background-image: url(src/assets/footer-bg.jpg);
    background-size: cover;
}

#socials-footer {
    width: 100%;
    height: 90px;
    justify-content: space-around;
}

.icons-cnt {
    gap: 20px;
}

span {
    color: #0282f9;
    font-weight: bold;
}

</style>