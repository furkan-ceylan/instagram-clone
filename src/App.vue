<template>
  <div id="app">
    <Header />
    <main class="main">
      <Container>
        <router-view />
      </Container>
    </main>
  </div>
</template>

<script>
import Header from "./components/Header";
import CustomText from "./components/CustomText";
import Container from "./components/Container.vue";

export default {
  name: "App",
  components: {
    Header,
    CustomText,
    Container,
  },
};
</script>

<style scoped>
.main {
  padding-top: 40px;
  background-color: rgb(250, 250, 250);
}
</style>
