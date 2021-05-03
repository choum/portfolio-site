<template>
  <div class="md-layout-item">
    <md-card :class="{ largerCard: isJob }">
      <md-card-media-cover>
        <md-card-media :style="cssProps">
          <img :src="src" :class="{ largerCard: isJob }" />
        </md-card-media>
        <md-card-area :class="{ largerCard: isJob }">
          <md-card-header>
            <md-button
              v-if="isJob === false && isHidden === false"
              class="md-icon-button md-raised link md-accent"
              md-ripple="false"
            >
              <md-icon>launch</md-icon>
            </md-button>
            <p class="md-title">
              {{ title }}
            </p>
          </md-card-header>
          <md-card-expand>
            <md-card-expand-trigger>
              <md-button
                class="md-icon-button"
                @click.native="isHidden = !isHidden"
              >
                <md-icon>keyboard_arrow_down</md-icon>
              </md-button>
            </md-card-expand-trigger>
            <md-card-expand-content>
              <p class="md-body-1">
                {{ content }}
              </p>
            </md-card-expand-content>
          </md-card-expand>
        </md-card-area>
      </md-card-media-cover>
    </md-card>
  </div>
</template>

<script>
import Vue from "vue";
import VueMaterial from "vue-material";
import "vue-material/dist/vue-material.min.css";
import "vue-material/dist/theme/default.css";

Vue.use(VueMaterial);
export default {
  name: "ResumeCard",
  props: ["title", "content", "src", "isJob", "color", "link"],
  computed: {
    cssProps() {
      return {
        "--color": this.color
      };
    }
  },
  data: function() {
    return {
      isHidden: true
    };
  }
};
</script>

<style scoped lang="scss">
@import "../scss/_variable.scss";
.md-title {
  font-weight: bold;
}
.md-card-header {
  width: 100%;
}
.md-body-1 {
  font-size: 16px;
}
.md-card,
img,
.md-card-area {
  max-height: 250px !important;
  min-height: 250px !important;
}

.largerCard {
  min-height: 275px !important;
  max-height: 275px !important;
}

.md-card-area {
  justify-content: center !important;
  align-items: center !important;
}

img {
  filter: brightness(90%);
}

.md-expand-active .md-card-media {
  filter: brightness(70%);
}

.md-card-expand-content {
  margin-left: 1em;
  margin-right: 1em;
}

.md-card-expand i {
  color: #fff !important;
  font-size: 50px !important; /* Preferred icon size */
}

i {
  color: #fff !important;
}

.md-card-media {
  background-color: var(--color);
}
a {
  color: #fff !important;
  text-decoration: none;
  letter-spacing: 0.15em;
  display: inline-block;
  padding: 15px 20px;
  position: relative;
  margin-left: 11em !important;
  margin-right: 11em !important;
}
a:hover {
  text-decoration: none;
}
a:after {
  background: none repeat scroll 0 0 transparent;
  bottom: 2;
  content: "";
  display: block;
  height: 2px;
  left: 50%;
  position: absolute;
  background: #fff;
  transition: width 0.3s ease 0s, left 0.3s ease 0s;
  width: 0;
}
a:hover:after {
  width: 100%;
  left: 0;
}
.link {
  align-self: flex-end;
}
</style>
