<template>
  <div id="app">
    
    <TheHeader />
    <TheHome />
    <TheFooter />
    
  </div>
</template>

<script>
import './styles/global.css';
import TheHeader from './components/Header';
import TheHome from './pages/Home';
import TheFooter from './components/Footer.vue';


export default {
  name: 'App',
  components: {
    TheHeader,
    TheHome,
    TheFooter
}
}
</script>

