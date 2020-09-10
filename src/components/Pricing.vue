<template>
  <div id="pricing">
    <h1>Our Pricing</h1>
    <br>
    <div class="toggle-container">
      Annually
      <span class="plans icon" v-if="planToggle === true" v-on:click="changePlan"><i class="fal fa-toggle-off"></i></span>
      <span class="plans icon" v-else v-on:click="changePlan" ><i class="fal fa-toggle-on"></i></span>
      Monthly
    </div>
    <div class="card is-centered">
        <div class="card-content is-centered">
          Basic
          <br>
          <h2 v-if="planToggle === true">$ 19.99</h2>
          <h2 v-else class="is-vcentered">$ <span class="amount"> 199.99</span></h2>
          <hr>
          500 GB Storage
          <hr>
          2 Users Allowed
          <hr>
          Send up to 3 GB
          <hr>
          <button class="button">Learn More</button>
      </div>
    </div>

<!--    Professional-->
<!--    $24.99 $249.99-->
<!--    1 TB Storage-->
<!--    5 Users Allowed-->
<!--    Send up to 10 GB-->
<!--    Learn More-->

<!--    Master-->
<!--    $39.99 $399.99-->
<!--    2 TB Storage-->
<!--    10 Users Allowed-->
<!--    Send up to 20 GB-->
<!--    Learn More-->
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
  methods: {
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
  padding: 10px;
}

h1 {
  font-weight: bolder;
  font-size: 2em;
}

.toggle-container {
  margin: 5px;
}

.plans {
  margin: 5px;
}

.card {
  width: 90%;
  text-align: center;
  font-weight: bold;
  font-size: 1.2em;
  border-radius: 10px;
}

.amount {
  font-size: 2em;
  font-weight: bolder;
}

.button {
  background-color: #EAA466;
}

button:active {
  background-color: transparent;
}
</style>
