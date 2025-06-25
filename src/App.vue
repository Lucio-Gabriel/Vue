<template>
  <TheHeader v-show="showHeader" />

  <div v-show="showName">
    Nome: {{ firstName }} <br>
    Sobrenome: {{ lastName }}
  </div>

  <div v-if="accessLevel === 'admin'">Usuario: Admin</div>
  <div v-else-if="accessLevel === 'marketing'">Usuario: Marketing</div>
  <div v-else>Usuario Normal</div>

  <br>
  <hr>

   <TheSection />
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheSection from './components/TheSection.vue';

export default {
  name: 'App',
  components: {
    TheHeader,
    TheSection,
  },
  // Variaveis reativas
  data() {
    return {
      showHeader: true,
      firstName: "Jon",
      lastName: "Snow",
      showName: true,
      accessLevel: "admin"
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px;
}
</style>
