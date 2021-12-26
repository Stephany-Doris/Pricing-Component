<template>
  <h1>Our Pricing</h1>
  <p>Only pay for what you need</p>
  <div class="card-wrapper">
    <PricingCard title="Free">
      <span>$24.99</span>
      <ul>
        <li>storage</li>
      </ul>
    </PricingCard>
    <PricingCard title="Basic" />
    <PricingCard title="Pro" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import PricingCard from "./components/PricingCard.vue";

export default defineComponent({
  name: "App",
  setup() {},
  components: {
    PricingCard,
  },
});
</script>

<style>
#app {
  font-family: "Roboto", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 3em;
  font-size: 18px !important;
}

.card-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  column-gap: 2em;
  padding: 20px;
  max-width: inherit;
}
span {
  font-size: 2em;
}
ul {
  list-style: none;
  padding: 12px;
  border-top: 1px solid #eee;
  border-bottom: 1px solid #eee;
}

.card:hover span {
  font-size: 3em;
}

.card:hover ul {
  border-top: 1px solid #2e2f30;
  border-bottom: 1px solid #2e2f30;
}
</style>
