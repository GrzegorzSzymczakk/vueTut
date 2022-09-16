<template>
  <div>
    <div class="row">
      <input v-model.number="num1" type="number"/>
      <span>+</span>
      <input v-model.number="num2" type="number"/>
      <span>=</span>
      <span> {{ num1 + num2 }}</span>
    </div>
    <select v-model="food">
      <option>Taco</option>
      <option>Burito</option>
    </select>
    <div class="row second">
      <p v-if="food">My fav food is {{ food }}</p>
    </div>
  </div>

</template>

<script>
export default {
  name: "Calculator",
  data() {
    return {
      num1: 0,
      num2: 0,
      food: ''
    }
  }
}
</script>

<style scoped>

</style>