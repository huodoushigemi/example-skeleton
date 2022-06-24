<script setup>
import Exmaple1 from './exmaple1.vue'
import Exmaple2 from './exmaple2.vue'
import Exmaple3 from './exmaple3.vue'
</script>

<template>
  <div class="flex-wrap main">
    <Exmaple1 />
    <Exmaple2 />
    <Exmaple3 />
  </div>
</template>

<style>
  html, body {
    padding: 0;
    margin: 0;
    background: #f4f5f7;
  }
  div {
    box-sizing: border-box;
  }
  .row {
    display: flex;
  }
  .col {
    display: flex;
    flex-direction: column;
  }
  .flex-wrap {
    display: flex;
    flex-wrap: wrap;
  }
  .flex1 {
    flex: 1;
  }
</style>

<style scoped>
  .main > * {
    margin: 14px auto;
  }
</style>