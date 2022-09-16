<template>
  <div>
    <h3>What is your favourite kind of taco?</h3>
    <textarea v-model="tacos"></textarea>
    <br>
    <button v-show="tacos"
            type="submit">Let us know!
    </button>
  </div>
</template>

<script>
export default {
  name: "SingleButton",
  data(){
    return{
      tacos: ''
    }
  }
}
</script>

<style scoped>

</style>