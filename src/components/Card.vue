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
  color: #fff;
}

a:hover {
  text-decoration: none !important;
  text-transform: uppercase;
  color: #fff;
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

@media screen and (min-width: 650px) {
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
}
</style>