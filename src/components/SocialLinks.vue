<template>
  <div id="socialBar">
    <a href="https://github.com/choum" target="_blank">
      <font-awesome-icon
        :icon="['fab', 'github']"
        size="2x"
        class="space"
        :style="{ color: '#9c9c9c' }"
      />
      <md-tooltip md-direction="top">Github</md-tooltip>
    </a>
    <a
      href="https://www.linkedin.com/in/heather-tran-97092a108/"
      target="_blank"
    >
      <font-awesome-icon
        :icon="['fab', 'linkedin']"
        size="2x"
        class="space"
        :style="{ color: '#9c9c9c' }"
      />
      <md-tooltip md-direction="top">Linkedin</md-tooltip>
    </a>
    <a href="https://www.instagram.com/heathereats/" target="_blank">
      <font-awesome-icon
        :icon="['fab', 'instagram']"
        size="2x"
        :style="{ color: '#9c9c9c' }"
        class="space"
      />
      <md-tooltip md-direction="top">Instagram</md-tooltip>
    </a>
    <a href="../assets/Resume.pdf">
      <font-awesome-icon
        :icon="['far', 'file-pdf']"
        size="2x"
        :style="{ color: '#9c9c9c' }"
        class="space"
      />
      <md-tooltip md-direction="top">Resume</md-tooltip>
    </a>
    <a href="mailto:heathertran@rocketmail.com">
      <font-awesome-icon
        :icon="['far', 'envelope']"
        size="2x"
        :style="{ color: '#9c9c9c' }"
      />
      <md-tooltip md-direction="top">Email</md-tooltip>
    </a>
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
import { faFilePdf, faEnvelope } from "@fortawesome/free-regular-svg-icons";
library.add(faLinkedin, faInstagram, faGithub, faFilePdf, faEnvelope);
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
  margin-right: 15px;
}
.md-tooltip {
  margin-bottom: 2px;
  margin-right: 8px;
}
</style>
