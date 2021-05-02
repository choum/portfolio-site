<template>
  <md-card>
    <md-card-header class="md-display-2">
      <p>{{ title }}</p>
    </md-card-header>
  </md-card>
</template>
<script>
import Vue from "vue";
import VueMaterial from "vue-material";
import "vue-material/dist/vue-material.min.css";
import "vue-material/dist/theme/default.css";

Vue.use(VueMaterial);
export default {
  name: "TitleCard",
  props: ["title"]
};
</script>

<style scoped lang="scss">
@import "../scss/_variable.scss";
p {
  margin: 0px;
  text-shadow: 3px 2px #9c9c9c;
}
.md-card {
  margin-top: 2em;
  width: 50%;
  background-color: $babypink !important;
}
.md-display-2 {
  color: white !important;
  text-align: left;
  margin-left: 20px;
  font-size: 30pt;
  font-family: "Lato";
  font-weight: 700;
}

p:after {
  background: none repeat scroll 0 0 transparent;
  bottom: 0;
  content: "";
  display: block;
  height: 5px;
  left: 50%;
  position: absolute;
  background: #fff;
  transition: width 0.3s ease 0s, left 0.3s ease 0s;
  width: 0;
}
p:hover:after {
  width: 100%;
  left: 0;
  top: -5;
}
</style>
