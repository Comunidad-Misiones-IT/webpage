<template>
  <div id="app" class="container-fluid">

    <div class="mb-2">
      <button type="button" class="btn" onclick="cambiarModo()">🌞|🌚</button>
    </div>

    <img :src="avy" class="avatar" id="img" alt="avatar" />
    <h1>{{ msg }}</h1>

  <div class="desc">
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

  </div>
</template>


<script>
import avy from './assets/mit.png'
import instagram from './assets/instagram.png'
import twitter from './assets/twitter.png'
import discord from './assets/discord.png'
import linkedin from './assets/linkedin.png'
import youtube from './assets/youtube.png'
import github from './assets/github.png'
import email from './assets/email.png'

export default {
  name: 'app',
  data () {
    return {
      msg: 'Misiones IT',
      Twitter: twitter,
      Instagram: instagram,
      Discord: discord,
      Linkedin: linkedin,
      Youtube: youtube,
      Github: github,
      Email: email,
      avy: avy
    }
  }
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

.oscuro button {
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

.oscuro #img { 
  filter: invert(1) grayscale(100%) brightness(2);
}

.oscuro #link { 
  background-color: #ffffff;
}

.oscuro #ico { 
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

button:hover {
  color: #f1eded;
}

button:focus {
  outline:0;
}

* {
  background-color: transparent;
}

.links {
  padding: 0.2em 1.6em;
}

.link {
  margin: 0.5em;
  padding: 0.6em;
  font-weight: bold;
  border-radius: 25px;
}

.link:nth-child(even) {
  background-color: #76489a;
}

.link:nth-child(odd) {
  background-color: #643786;
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

.footer {
  display: flex;
  justify-content: center;
  background-color: transparent;
  color: #3c373b;
  font-size: 14px;
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

  .desc {
    margin: 4em;
  }
}

@media screen and (max-width: 650px) { 
  .ico {
    width: 30px;
  }

  .desc {
    margin: 2em;
  }
}
</style>