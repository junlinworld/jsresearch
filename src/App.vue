<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <question/> -->
    <queTitle />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import category from '@/components/category.vue'
import question from '@/components/question.vue'
import answer from '@/components/answer.vue'
import queTitle from '@/components/quetitle.vue'

export default {
  name: 'app',
  components: {
    question,
    queTitle,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
