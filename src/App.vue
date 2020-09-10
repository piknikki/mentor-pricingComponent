<template>
  <div id="app">
    <img class="logo" alt="Aroma Therapy Logo" src="./assets/aromatherapy.png">
    <span class="aroma">AROMA</span>
    <span class="therapy">therapy</span>
    <Pricing />
  </div>
</template>

<script>
import Pricing from '@/components/Pricing'

export default {
  name: 'App',
  components: {
    Pricing
  }
}
</script>

<style>
#app {
  font-family: 'Trocchi', serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #D8E0E3;
  color: #2c3e50;
  margin-top: 60px;
}

.logo {
  width: 50px;
}

.aroma {
  color: white;
  font-family: 'IBM Plex Sans', sans-serif;
  font-weight: bold;
  margin: 0 5px;
  letter-spacing: 2px;
}

.therapy {
  color: #EAA466;
}

</style>
