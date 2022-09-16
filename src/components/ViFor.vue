<template xmlns="http://www.w3.org/1999/html">
  <ul>
    <li v-for="num in 7"
        :key="num">
        {{ num }}

        </li>
  </ul>
</template>

<script>
export default {
  name: "ViFor"
}
</script>

<style scoped>

</style>