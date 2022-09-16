<template>

  <div class="item">
    <div class="quantity">
      <button class="inc" @click="counter > 0 ? counter -= 1 : 0">---</button>
      <span  class="quant-text inc">Quantity: {{ counter }}</span>
      <button class="inc" @click="counter += 1">+++ </button>
    </div>
    <button class="submit" @click="counter = 0">Submit</button>
  </div>
</template>

<script>
export default {
  name: "VOn",
  data() {
    return {
      counter: 0
    }
  }
}
</script>

<style scoped>

.inc{
  color: red;
}


</style>