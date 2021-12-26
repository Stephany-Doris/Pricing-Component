<template>
  <div class="card">
    <h2>{{ title }}</h2>
    <slot></slot>
    <Button text="Subscribe" />
  </div>
</template>

<script>
import { defineComponent } from "vue";
import Button from "./Button.vue";

export default defineComponent({
  name: "PricingCard",
  props: {
    title: String,
  },
  components: { Button },
  setup() {},
});
</script>

<style scoped>
.card {
  height: 450px;
  width: -webkit-fill-available;
  background-color: white;
  color: #050710;
  border-radius: 8px;
  margin: auto;
  padding: 8px;
  position: relative;
}

.card:hover {
  height: 500px;
  /* flex-grow: 2; */
  color: white;
  background-color: #050710;
}
</style>