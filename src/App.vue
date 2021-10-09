<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-brand href="#">Rick And Morty</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="#">Inicio</b-nav-item>
          <b-nav-item href="#">Buscar</b-nav-item>
          <b-nav-item href="#">acerca de</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <main>
      <b-container>
        <b-row>
          <b-col cols="4" v-for="(personaje, index) in personajes" :key="index">
            <b-card
              :title="personaje.nombre"
              :img-src="personaje.imagen"
              img-alt="Image"
              img-top
              tag="article"
              style="max-width: 20rem"
              class="mb-2 mt-2"
            >
            </b-card>
          </b-col>
        </b-row>
      </b-container>
    </main>
  </div>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    personajes: [
      {
        id: 1,
        nombre: "Morty",
        imagen: "https://rickandmortyapi.com/api/character/avatar/2.jpeg",
      },
      {
        id: 2,
        nombre: "Rick",
        imagen: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
      },
      {
        id: 3,
        nombre: "Summer",
        imagen: "https://rickandmortyapi.com/api/character/avatar/3.jpeg",
      },
      {
        id: 4,
        nombre: "Beth",
        imagen: "https://rickandmortyapi.com/api/character/avatar/4.jpeg",
      },
      {
        id: 5,
        nombre: "Jerry",
        imagen: "https://rickandmortyapi.com/api/character/avatar/5.jpeg",
      },
    ],
  }),
};
</script>

<style></style>
