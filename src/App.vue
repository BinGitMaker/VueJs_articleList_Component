<style>
@import './assets/base.css';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<template class="app">
  

    <div id="app">
      <h1>{{message}}</h1>
      <Accueil />
    </div>


  
</template>

<script>
import Accueil from './components/Accueil.vue'

export default {
  name: 'App',
  components: {
    Accueil,
  },
  data() {
    return{
      message: 'Welcome to my Article List'
    }
  },
  
}
</script>


