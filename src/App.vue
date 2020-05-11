<template>
  <div id="app" :style="backgroundStyle" >
    <appHeader :bgColor="backgroundStyle.background"></appHeader>
    <main class="main">
        <h1 class="header">Generate a color!</h1>
        <button class="button" @click="getNewRGBColor">Generate</button>
    </main>
  </div>
  
</template>

<script>

import Header from './components/Header.vue';

export default {
    data() {
        return {
            backgroundStyle: {
                background: `rgb (255,255,255)`
            },
            buttonStyle: {
                color: '',
                border: '',
            }
            
            
        }
    },
    methods: {
        getNewRGBColor() {
            const getRandomRed = Math.floor(Math.random() * 255 + 1);
            const getRandomGreen = Math.floor(Math.random() * 255 + 1);
            const getRandomBlue = Math.floor(Math.random() * 255 + 1);
            const getRandomRGB = `${getRandomRed}, ${getRandomGreen}, ${getRandomBlue}`;
            console.log(getRandomRGB);
            this.backgroundStyle.background = `rgb(${getRandomRGB})`
        }
    },
    watch: {
        changeFontColor() {
            return this.fontColor = `rgb(255,255,255)`;
        }
    },
    components: {
        appHeader: Header,
    },
}

</script>

<style>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}
#app {
    height: 100vh;
}

.main {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 50%;
}

.button {
    font-size: 3rem;
    background: transparent;
    border: 2px solid black;
    padding: 20px;
    margin: 20px;
}

.button:hover {
    cursor: pointer;
    background: black;
    color: white;
}

</style>
