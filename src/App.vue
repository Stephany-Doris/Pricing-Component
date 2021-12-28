<template>
  <h1>Our Pricing</h1>
  <p>Only pay for what you need</p>
  <div class="card-wrapper">
    <PricingCard title="Free" price="$0.00">
      <ul>
        <li v-for="(item, index) in pricingDetails" :key="index">
          <div v-for="value in item" :key="value">
            <div class="list-item" v-if="index === 0">{{ value }}</div>
          </div>
        </li>
      </ul>
    </PricingCard>
    <PricingCard title="Basic" price="$9.99">
      <ul>
        <li v-for="(item, index) in pricingDetails" :key="index">
          <div v-for="value in item" :key="value">
            <div class="list-item" v-if="index === 1">{{ value }}</div>
          </div>
        </li>
      </ul>
    </PricingCard>
    <PricingCard title="Pro" price="$24.99">
      <ul>
        <li v-for="(item, index) in pricingDetails" :key="index">
          <div v-for="value in item" :key="value">
            <div class="list-item" v-if="index === 2">{{ value }}</div>
          </div>
        </li>
      </ul>
    </PricingCard>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import PricingCard from "./components/PricingCard.vue";

export default defineComponent({
  name: "App",
  setup() {
    const pricingDetails = [
      {
        users: "1 users",
        storage: "5GB storage",
        downloads: "10 downloads per month",
      },
      {
        users: "1 users",
        storage: "25GB storage",
        downloads: "unlimited downloads",
        community: "Join Slack community",
      },
      {
        users: "4 users",
        storage: "125GB storage",
        downloads: "unlimited downloads",
        community: "Join Slack community",
        support: "24/7 customer support",
      },
    ];

    return {
      pricingDetails,
    };
  },
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
  margin: 0 10em;
}
span {
  font-size: 1.8em;
}

ul {
  list-style: none;
  padding: 2em 3em 0;
}
.list-item {
  border-bottom: 1px solid #eee;
  padding: 10px 0;
  font-size: 15px;
}

.card:hover span {
  font-size: 2.5em;
}

.card:hover .list-item {
  border-top: 1px solid #2e2f30;
  border-bottom: 1px solid #2e2f30;
}
</style>
