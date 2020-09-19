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
.oscuro { 
    background-color: #1f1f1f; 
    color: #f1eded;
}

.oscuro h1 { 
    color: #f1eded;
}

.oscuro sup {
    color: #f1eded;
}

.oscuro a {
    color: #3c373b;
}

.oscuro a:hover {
  text-decoration:none;
  text-transform: uppercase;
  color: #3c373b;
}

.oscuro .img { 
  filter: invert(1) grayscale(100%) brightness(2);
}

.oscuro .link { 
  background-color: #ffffff;
}

.oscuro .ico { 
  filter: sepia(100%) hue-rotate(40deg) invert(1) grayscale(20%) saturate(50%) brightness(7);
}

.oscuro .desc {
  color: white;
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

* {
  background-color: transparent;
}

.avatar {
  width: 7em;
  margin-bottom: 1em;
  margin-top: 0.2em;
}

h1, h2 {
  font-weight: normal;
  font-size: 2.5rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 30px;
}

a {
  color: #ffffff;
}

a:hover {
  text-decoration:none;
  text-transform: uppercase;
  color: #ffffff;
}

@media screen and (min-width: 650px) {
  .links {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }

  .ico {
    width: 50px;
  }

  a {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
}

@media screen and (max-width: 650px) { 
  .ico {
    width: 30px;
  }
}
</style>