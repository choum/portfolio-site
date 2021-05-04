<template>
  <div
    class="md-layout-item md-medium-size-33 md-small-size-50 md-xsmall-size-100"
  >
    <md-card :class="{ largerCard: isJob }">
      <md-card-media-cover>
        <md-card-media :style="cssProps">
          <img :src="src" :class="{ largerCard: isJob }" />
        </md-card-media>
        <md-card-area :class="{ largerCard: isJob }">
          <md-card-header>
            <md-button
              :href="link"
              v-if="isJob === false && isHidden === false"
              class="md-icon-button md-raised link md-accent"
              md-ripple="false"
            >
              <md-icon>launch</md-icon>
            </md-button>
            <p class="md-title">
              {{ title }}
            </p>
            <span class="date" v-if="begin !== undefined && end !== undefined"
              >{{ begin }} - {{ end }}</span
            >
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
  props: ["title", "content", "src", "isJob", "color", "link", "begin", "end"],
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
  margin-top: 0px !important;
}
.md-card-header {
  width: 100%;
  padding-bottom: 8px;
  padding-top: 8px;
}
.md-body-1 {
  font-size: 16px;
}
@media (max-width: 415px) {
  .md-body-1 {
    font-size: 14px !important;
  }
  .md-icon {
    color: #fff !important;
    font-size: 25px !important;
  }
  .md-title {
    font-size: 20px;
  }
  .md-card-expand.md-icon-button {
    width: 25px;
    height: 25px;
  }
  .md-card,
  img,
  .md-card-area {
    max-height: 325px !important;
    min-height: 325px !important;
  }
}
img {
  object-fit: cover;
}
.md-card,
img,
.md-card-area {
  max-height: 250px;
  min-height: 250px;
}

.largerCard {
  min-height: 275px;
  max-height: 275px;
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
.link {
  align-self: flex-end;
}
.date {
  font-style: italic;
}
.md-card {
  margin-bottom: 3em;
}
</style>
