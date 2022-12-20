<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    <h1>Before</h1>
    <div>
      <Formik />

    </div>
    <h1>After</h1>

  </div>

</template>

<script setup>
import Formik from "./components/formik-form.vue";

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
