<script>
import AppFeatures from './AppFeatures.vue';

export default {
    name: 'AppMain',
    components: {
    AppFeatures
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
                <li class="links" v-for="currentLink in linkList.list">
                    {{ currentLink }}
                </li>
            </ul>
        </div>
    </div>
    
  </div>

  <div id="empty-bar" class="my-display">

    CONTENUTO VUOTO DA RIEMPIRE DOMANII.
        
  </div>

  <AppFeatures></AppFeatures>

</template>

<style>

/*Regole da creare successivamente come variabili SaSS
perchè molto riusabili.*/
.bar {
    width: 100%;
    height: 140px;
}

.my-display {
    display: flex;
    align-items: center;
}

.text {
    color: black;
}

.links {
    list-style: none;
    border-bottom: 8px solid transparent;
    margin-top: 54px;
    padding-bottom: 54px;
    &:hover {
        color: #0282f9;
        cursor: pointer;
        border-bottom: 8px solid #0282f9;
    }
}

/*Regole normali.*/

#navbar {
    background-color: white;
    font-weight: bold;
    justify-content: space-around;
}

#nav-list {
    display: flex;
    gap: 20px;
}

#empty-bar {
    font-weight: bold;
    width: 100%;
    height: 160px;
    justify-content: center;
}

</style>