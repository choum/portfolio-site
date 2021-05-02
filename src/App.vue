<template>
  <div id="app">
    <link
      rel="stylesheet"
      href="//fonts.googleapis.com/css?family=Roboto:400,500,700,400italic|Material+Icons"
    />
    <link
      rel="stylesheet"
      href="//fonts.googleapis.com/css?family=Lato:400,500,700,400italic|Material+Icons"
    />
    <Header />
    <main>
      <div class="row md-layout md-gutter">
        <div class="md-layout-item"><Welcome /></div>
      </div>
      <div class="md-layout-md-gutter">
        <div class="md-layout-item"><IntroCard /></div>
      </div>
      <ResumeRow />
    </main>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Welcome from "./components/Welcome.vue";
import IntroCard from "./components/IntroCard.vue";
import ResumeRow from "./components/ResumeRow.vue";
export default {
  name: "App",
  components: {
    Header,
    Welcome,
    IntroCard,
    ResumeRow
  }
};
</script>

<style lang="scss">
@import "scss/_variable.scss";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.row {
  margin-left: 0 !important;
}
main {
  margin-left: 10vw !important;
  margin-right: 10vw !important;
  height: 100%;
}
body {
  background-color: $champagnepink;
  width: 100%;
  padding-bottom: 1px;
}
</style>

<style lang="scss">
@import "~vue-material/dist/theme/engine"; // Import the theme engine

@include md-register-theme(
  "default",
  (
    primary: #fec5bb,
    // The primary color of your brand
      accent: #f8edeb // The secondary color of your brand
  )
);

@import "~vue-material/dist/theme/all"; // Apply the theme
</style>
