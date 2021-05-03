<template>
  <div id="app">
    <Header />
    <main class="main">
      <Container>
        <router-view />
      </Container>
    </main>
          <Container>
    <footer>
      <Footer />
    </footer>
    </Container>
  </div>
</template>

<script>
import Header from "./components/Header";
import CustomText from "./components/CustomText";
import Container from "./components/Container.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    CustomText,
    Container,
    Footer
  },
};
</script>

<style scoped>
.main {
  padding-top: 40px;
  background-color: rgb(250, 250, 250);
}
</style>
