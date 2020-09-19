<template>
  <div class="link">
    <a v-bind:href="link_src">
      <img v-bind:src="img_src" class="ico"/>
      {{ nombre }}
    </a>
  </div>
</template>


<script>
  export default {
    name: "Card",
    props: {
      nombre: String,
      img_src: String,
      link_src: String
    }
  }
</script>

<style>
a {
  color: #fff !important;
}

.oscuro a {
  color: #3c373b !important;
}

a:hover {
  text-decoration: none !important;
  text-transform: uppercase;
  color: #fff;
}

.oscuro a:hover {
  text-decoration:none;
  text-transform: uppercase;
  color: #3c373b;
}

.oscuro .link { 
  background-color: #fff !important;
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

.oscuro .ico { 
  filter: sepia(100%) hue-rotate(40deg) invert(1) grayscale(20%) saturate(50%) brightness(7);
}

@media screen and (min-width: 650px) {
  .links {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }

  a {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
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
}

@media screen and (max-width: 650px) { 
  .ico {
    width: 30px;
  }
}
</style>