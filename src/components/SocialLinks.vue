<template>
  <div id="socialBar">
    <font-awesome-icon
      :icon="['fab', 'github']"
      size="2x"
      class="space"
      :style="{ color: '#9c9c9c' }"
    />
    <font-awesome-icon
      :icon="['fab', 'linkedin']"
      size="2x"
      class="space"
      :style="{ color: '#9c9c9c' }"
    />
    <font-awesome-icon
      :icon="['fab', 'instagram']"
      size="2x"
      :style="{ color: '#9c9c9c' }"
    />
  </div>
</template>

<script>
import Vue from "vue";
import {
  faGithub,
  faLinkedin,
  faInstagram
} from "@fortawesome/free-brands-svg-icons";
import { library } from "@fortawesome/fontawesome-svg-core";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
library.add(faLinkedin, faInstagram, faGithub);
Vue.component("font-awesome-icon", FontAwesomeIcon);
export default {
  name: "SocialLinks"
};
</script>

<style scoped>
#socialBar {
  margin-top: 1.5em;
}
.space {
  margin-right: 10px;
}
</style>
