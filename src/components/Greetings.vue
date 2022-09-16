<template>
  <p> {{ word }}</p>
</template>

<script lang="ts">
import {defineComponent} from "vue";
export default defineComponent( {
  name: "Greetings",
  data(){
    const word = "Hey";
    return {word};
  }
})
</script>

<style scoped>

</style>