<template>
  <div>
  <HelloWorld>First component not working</HelloWorld>
  <SecondComponent>Second component not working</SecondComponent>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import SecondComponent from './components/SecondComponent.vue'
export default {
  components: { HelloWorld, SecondComponent },
  
}
</script>

<style>
  body{
    text-align: center;
  }
</style>