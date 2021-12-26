<template>
  <button class="button">
    {{ text }}
  </button>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "Button",
  props: {
    text: String,
  },
  setup() {},
});
</script>

<style scoped>
.button {
  width: 70%;
  color: white;
  background-color: #050710;
  border: 2px solid white;
  height: 40px;
  border-radius: 18px;
  bottom: 10%;
  position: absolute;
  left: 15%;
  font-size: inherit;
}

.card:hover .button {
  color: #050710;
  background-color: white;
  border: 2px solid #050710;
}
</style>