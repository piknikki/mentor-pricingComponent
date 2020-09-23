<template>
  <div id="pricing">
    <h1>Our Pricing</h1>
    <br>
    <div class="toggle-container tabs is-centered is-medium">
      <div v-if="planToggle" class="is-centered">
        <span class="on">Monthly</span>
          <span class="toggle" @click="planToggle = !planToggle">
            <font-awesome-icon :icon="['fal', 'toggle-off']" />
          </span>
        <span class="off">Annually</span>
      </div>

      <div v-else class="is-centered">
        <span class="off">Monthly</span>
          <span class="toggle" @click="planToggle = !planToggle">
            <font-awesome-icon :icon="['fal', 'toggle-on']" />
          </span>
        <span class="on">Annually</span>
      </div>

    </div>
    <div class="cards-container columns">
      <div class="card column is-3 is-desktop">
          <div class="card-content">
            Basic
            <br>
            <h2 v-if="planToggle === true">$ <span class="amount"> 19.99</span></h2>
            <h2 v-else >$ <span class="amount"> 199.99</span></h2>
            <hr>
            500mL therapy
            <hr>
            2 Scents Allowed
            <hr>
            Share up to 100mL
            <hr>
            <button class="button">Learn More</button>
        </div>
      </div>

      <div class="card column middle-plan is-3 is-desktop">
        <div class="card-content">
          Professional
          <br>
          <h2 v-if="planToggle === true">$ <span class="amount"> 24.99</span></h2>
          <h2 v-else >$ <span class="amount"> 249.99</span></h2>
          <hr>
          1000mL therapy
          <hr>
          5 Scents Allowed
          <hr>
          Share up to 300mL
          <hr>
          <button class="button">Learn More</button>
        </div>
      </div>

      <div class="card column is-3 is-desktop">
        <div class="card-content">
          Master
          <br>
          <h2 v-if="planToggle === true">$ <span class="amount"> 39.99</span></h2>
          <h2 v-else >$ <span class="amount"> 399.99</span></h2>
          <hr>
          2000mL therapy
          <hr>
          10 Scents Allowed
          <hr>
          Share up to 500mL
          <hr>
          <button class="button">Learn More</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Pricing',
  data () {
    return {
      planToggle: false
    }
  },
  watch: {
    changePlan () {
      this.planToggle = !this.planToggle
    }
  }
}
</script>

<style>
#pricing {
  font-family: 'IBM Plex Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  //background-image: url("../assets/bg-top.svg");
  background-color: #F7F7FF;
  margin: 30px;
  border-radius: 10px;
  padding: 10px 50px 40px;
}

h1 {
  font-weight: bolder;
  font-size: 2em;
}

.toggle-container {
  margin: auto;
  text-align: center;
  font-size: 1.6em;
  padding: 30px;
}

.toggle {
  margin: 10px;
  color: #8085E2;
}

.on {
  color: #8085E2;
}

.off {
  color: darkgray;
}

.card {
  width: 200px;
  text-align: center;
  font-weight: bold;
  font-size: 1.2em;
  border-radius: 10px;
  margin: 10px auto;
}

li {
  margin: 10px;
}

.middle-plan {
  background-color: #8085E2;
}

.card:hover {
  background-color: #8085E2;
}

.amount {
  font-size: 2em;
  font-weight: bolder;
}

.button {
  background-color: #EAA466;
  width: 70%;
}

button:active {
  background-color: transparent;
}

.cards-container {
  padding: 0 40px;
}

.card-content {
  padding: 2px 2px;
}
</style>
