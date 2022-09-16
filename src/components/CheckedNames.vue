<template>
  <div>
    <label for="john">John</label>
    <input id="john" type="checkbox" v-model="checkedNames" value="John">

    <label for="paul">Paul</label>
    <input id="paul" type="checkbox" v-model="checkedNames" value="Paul">

    <!--    <label for="george">George</label>-->
    <!--    <input id="george" type="checkbox" v-model="checkedNames" value="George">-->


    <input v-model="checkedNames">
  </div>
  <br/>
  <div>
    <span v-for="option in options"
          :key="option">
      <input v-model="checkedNames"
             :id="option.value"
             :value="option.value"
             type="checkbox">
      <label for="option.value"> {{ option.value }} </label>

    </span>
    <br>
    <span>Checked names: {{ checkedNames }}</span>
  </div>


</template>

<script>
export default {
  name: "CheckedNames",
  data() {
    return {
      checkedNames: [],
      options: [
        {value: 'John'},
        {value: 'Paul'},
        {value: 'George'},
        {value: 'Ringo'}
      ]
    }
  }
}
</script>

<style scoped>

</style>