<script setup>
import {defineProps} from "vue";
const props = defineProps({name: String, type: String});

const field_input = {
  template: `
  <input name=${props.name} type=${props.type}>
  </input>
  `
}


</script>

<template>
  <div id="field">
  <component :is="field_input"></component>
  </div>
</template>

<style scoped>

</style>