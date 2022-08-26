<template>
  <div id="app">
    
    <TheHeader />
    <TheHome />
    
  </div>
</template>

<script>
import './styles/global.css';
import TheHeader from './components/Header';
import TheHome from './pages/Home';


export default {
  name: 'App',
  components: {
    TheHeader,
    TheHome
}
}
</script>

