<template>
  <div class="md-layout-item">
    <md-card :class="{ largerCard: isJob }">
      <md-card-media-cover>
        <md-card-media :style="cssProps">
          <img :src="src" :class="{ largerCard: isJob }" />
        </md-card-media>
        <md-card-area :class="{ largerCard: isJob }">
          <md-card-header>
            <p class="md-title">
              {{ title }}
            </p>
          </md-card-header>
          <md-card-expand>
            <md-card-expand-trigger>
              <md-button class="md-icon-button">
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
  props: ["title", "content", "src", "isJob", "color"],
  computed: {
    cssProps() {
      return {
        "--color": this.color
      };
    }
  }
};
</script>

<style scoped lang="scss">
@import "../scss/_variable.scss";
.md-title {
  font-weight: bold;
}
.md-body-1 {
  font-size: 16px;
}
.md-card,
img,
.md-card-area {
  max-height: 200px !important;
}

.largerCard {
  min-height: 300px !important;
}

.md-card-area {
  justify-content: center;
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

.md-icon {
  color: #fff !important;
  font-size: 50px !important; /* Preferred icon size */
}

.md-card-media {
  background-color: var(--color);
}
</style>
