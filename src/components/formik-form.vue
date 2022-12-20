<script setup>
import {shallowRef} from "vue";
  const firstComponent = {
    template :`<div><h1>first component</h1></div>`};
  const secondComponent = {
    template: `<div><h1>second component</h1></div>`
  };
  const thirdComponent = {
    template: `<div><h1>third component</h1></div>`
  };
  const currentComponent = shallowRef({template:''});
  currentComponent.value = firstComponent;
  const componentsLooping = () => {
    if(currentComponent.value === firstComponent) {
      currentComponent.value = secondComponent;
    } else if (currentComponent.value === secondComponent) {
      currentComponent.value = thirdComponent;
    }else{
      currentComponent.value = firstComponent;
    }
  }

const name = 'formik name d';
</script>

<template>
  <div>
    <h1>{{name}}</h1>
    <button :onclick="componentsLooping" >click</button>
    <component :is="currentComponent" />

  </div>

</template>

<style scoped>

</style>