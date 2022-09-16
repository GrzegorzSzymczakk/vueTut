<script lang="ts">
import {defineComponent} from "vue";
import Greetings from './components/Greetings.vue';
import CheckedNames from "./components/CheckedNames.vue";
import SingleButton from "./components/SingleButton.vue";
import ViFor from "./components/ViFor.vue";
import VOn from "./components/VOn.vue";
import Calculator from "./components/Calculator.vue";
import Comments from "./components/Comments.vue";
import CompProperties from "./components/CompProperties.vue";

export default defineComponent({
  name: "App",
  components: {
    CompProperties,
    Comments,
    Calculator,
    ViFor,
    SingleButton,
    CheckedNames,
    Greetings,
    VOn

  },
  data() {
    const text: number = 23;
    return {text};
  }
})
</script>


<template>
  <br>

  <CompProperties/>

</template>

<style scoped>

</style>
