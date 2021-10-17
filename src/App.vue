<template>
  <div>
    <Navbar />
    <main>
      <Card />
    </main>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Card from "./components/Card.vue";
export default {
  name: "App",
  components: {
    Navbar,
    Card,
  },
};
</script>
