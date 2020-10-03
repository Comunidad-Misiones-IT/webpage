<template>
  <div id="app" class="container-fluid">

    <Header />
    <CardList />
    <Footer />

  </div>
</template>
<script>
import Header from './components/Header';
import CardList from './components/CardList';
import Footer from './components/Footer';
export default {
  name: 'app',
  components: {
    Header,
    CardList,
    Footer
  }, 
}
</script>

<style>
* {
  background-color: transparent;
}
#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-size: 100%;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #3c373b;
  margin: 0.4em 0em;
}
.oscuro { 
    background-color: #1f1f1f; 
    color: #f1eded;
}
.oscuro .img { 
  filter: invert(1) grayscale(100%) brightness(2);
}
</style>