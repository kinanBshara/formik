<script setup>
import {defineProps , withDefaults} from "vue";
const props = defineProps({name: String, type: String});

const input = {
  template: `
  <input name = ${props.name} type = ${props.type}>
  </input>
  `
}


</script>

<template>
  <div id="field">
  <component :is=input.template></component>
  </div>
</template>

<style scoped>

</style>