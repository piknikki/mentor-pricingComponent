<template>
  <div id="app">
    <div class="columns">
      <div class="column">
        <img id="logo" class="is-half" alt="Aroma Therapy Logo" src="./assets/aromatherapy.png">
      </div>
      <div id="name-block" class="column ">
        <div class="aroma has-text-centered">AROMA</div>
        <div class="therapy has-text-centered">therapy</div>
      </div>
    </div>
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
  padding: 30px 0;
  //background-color: #F7F7FF;
}

#logo {
  width: 75px;
}

.aroma {
  color: white;
  font-family: 'IBM Plex Sans', sans-serif;
  font-size: 1.8em;
  letter-spacing: 2px;
}

.therapy {
  color: #EAA466;
}

</style>
