<template>
  <div id="app">
    <div class="title-cont">
      <img alt="Vue logo" src="./assets/logo.png">
      <h2>A Vue Editor</h2>
    </div>
    
    <EditorContent/>
  </div>
</template>

<script>
import EditorContent from './components/EditorContent.vue'

export default {
  name: 'app',
  components: {
    EditorContent
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  margin-top: 60px;
}
.title-cont {
  text-align: center;
}
</style>
