<script>

export default {
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

</template>

<style>

/*Regole da creare successivamente come variabil SaSS
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

    /*&:hover {
        background-color: #0282f9;
    }*/
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

</style>