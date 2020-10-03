<template>
  <div id="app" class="container-fluid"
    <div class="mb-2">
      <button type="button" class="btn" onclick="cambiarModo()">🌞|🌚</button>
    </div>

    <img :src="avy" class="avatar" id="img" alt="avatar" />
    <h1>{{ msg }}</h1>

  <div class="m-2 desc">
    <p>Somos una comunidad convencida de que Misiones tiene talento valioso para la industria IT, y lo queremos potenciar. Si queres saber que hay detrás de esta pagina, manijear juegos o compartir experiencias seguí a MIT en sus redes:</p>
  </div>
 
    <div class="links container-fluid">
      <div class="link" id="link">
        <a href="https://discord.com/invite/6Tkv8pn">
          <img :src="Discord" class="ico" id="ico" alt="discord" />
          Discord
        </a>
      </div>
    
      <div class="link" id="link">
        <a href="https://www.instagram.com/comunidadmit/">
          <img :src="Instagram" class="ico" id="ico" alt="instagram" />
          <a>Instagram</a>
        </a>
      </div>   
      
      <div class="link" id="link">
        <a href="https://twitter.com/ComunidadMIT">
          <img :src="Twitter" class="ico" id="ico" alt="twitter" />
          Twitter
        </a>
      </div>

      <div class="link" id="link">
        <a href="https://www.linkedin.com/company/comunidad-mit/">
          <img :src="Linkedin" class="ico" id="ico" alt="linkedin" />
          Linkedin
        </a>
      </div>

      <div class="link" id="link">
        <a href="https://github.com/Comunidad-Misiones-IT">
          <img :src="Github" class="ico" id="ico" alt="github" />
          Github
        </a>
      </div>

      <div class="link" id="link">
          <a href="https://www.youtube.com/watch?v=tabBLNTPInQ">
            <img :src="Youtube" class="ico" id="ico" alt="youtube" />
           WEBINAR: Programar desde Misiones
          </a>
      </div>
    </div>

    <div class="footer container-fluid pt-3 pb-1">
      <sup>All rigths reserved | Comunidad MIT © 2020</sup>
    </div>

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

@media screen and (min-width: 650px) {
  .links {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }

  .link {
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 160px;
    width: 90%;
    border-radius: 15px;
    padding: 3em;
    background-color: transparent;
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

.oscuro .img { 
  filter: invert(1) grayscale(100%) brightness(2);
}

</style>