<template>
  <div class="wrapper">
    <md-card>
      <md-card-header>
        <md-avatar class="md-large">
          <img src="../assets/me.jpg" alt="Avatar" />
        </md-avatar>
      </md-card-header>

      <md-card-content>
        <p class="md-title">
          My name is Heather. I am currently a full-time software developer
          analyst at Northrop Grumman in Redondo Beach, California. I was born
          and raised in Orange County and has developed a great interest in web
          development and social media
        </p>
        <SocialLinks />
      </md-card-content>
    </md-card>
  </div>
</template>

<script>
import Vue from "vue";
import VueMaterial from "vue-material";
import SocialLinks from "./SocialLinks.vue";
import "vue-material/dist/vue-material.min.css";
import "vue-material/dist/theme/default.css";

Vue.use(VueMaterial);
export default {
  name: "IntroCard",
  components: { SocialLinks }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.md-avatar {
  float: none;
  margin-top: -75px;
  min-width: 125px;
  min-height: 125px;
  border-radius: 125px;
}
.md-card-header {
  padding-top: 0;
}
</style>
