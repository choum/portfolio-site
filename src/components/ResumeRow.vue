<template>
  <div id="overWrapper">
    <TitleCard title="Work History" icon="work" />
    <div class="md-layout md-gutter resumeWrapper">
      <!-- NG -->
      <ResumeCard
        :title="ng.title"
        :content="ng.content"
        :src="ng.src"
        :isJob="ng.isJob"
      />
      <!-- CPP -->
      <ResumeCard
        :title="cpp.title"
        :content="cpp.content"
        :src="cpp.src"
        :isJob="cpp.isJob"
      />
      <!-- EKGaming -->
      <ResumeCard
        :title="ek.title"
        :content="ek.content"
        :src="ek.src"
        :isJob="ek.isJob"
        :color="ek.color"
      />
      <!-- OpenAI -->
      <ResumeCard
        :title="oa.title"
        :content="oa.content"
        :src="oa.src"
        :isJob="oa.isJob"
      />
    </div>
    <TitleCard title="Projects" icon="code" />
    <div class="md-layout md-gutter resumeWrapper">
      <!-- project lite-->
      <ResumeCard
        :title="pl.title"
        :content="pl.content"
        :src="pl.src"
        :isJob="pl.isJob"
        :color="pl.color"
        :link="pl.link"
      />
      <!--bumpie-->
      <ResumeCard
        :title="bump.title"
        :content="bump.content"
        :src="bump.src"
        :isJob="bump.isJob"
        :color="bump.color"
        :link="bump.link"
      />
    </div>
  </div>
</template>
<script>
import Vue from "vue";
import VueMaterial from "vue-material";
import "vue-material/dist/vue-material.min.css";
import "vue-material/dist/theme/default.css";
import ResumeCard from "./ResumeCard.vue";
import TitleCard from "./TitleCard.vue";

Vue.use(VueMaterial);
export default {
  name: "ResumeRow",
  components: { ResumeCard, TitleCard },
  data() {
    return {
      ng: {
        title: "Northrop Grumman",
        content:
          "My name is Heather. I am currently a full-time software developer analyst at Northrop Grumman in Redondo Beach, California. I was born and raised in Orange County and has developed a great interest in web development and social media",
        src: require("../assets/ng.jpg"),
        isJob: true
      },
      cpp: {
        title: "Cal Poly Pomona",
        content:
          "I worked here during my time in college. Here I created mockups and implemented changes using HTML, CSS, Bootstrap, Javascript. I created components using React.js and Vue.js",
        src: require("../assets/cpp.jpeg"),
        isJob: true
      },
      ek: {
        title: "EKGaming",
        content:
          "This internship allowed me to learn how to work around Wordpress using code. Gaming is one of my favorite hobbies and working on this site with others let me enjoy my passion as well as be productive. I used basic HTML, CSS, Javascript/JQuery for this job. This position was remote.",
        src: require("../assets/ek.png"),
        isJob: true,
        color: "#fec89a"
      },
      oa: {
        title: "Open AI",
        content:
          "This is my first contractor position with a non-profit. Learn about how I helped artificial intelligence learn by playing video games.",
        src: require("../assets/openai.gif"),
        isJob: true
      },
      pl: {
        title: "Project Lite",
        content:
          "Project Lite was a project that some college buddies and I decided to do for the Bronco Startup Competition during my senior year at Cal Poly Pomona. This was a way for us to practice our development skills using React.js in a startup environment. As a finalist we were able to present to entrepreneurs.",
        src: require("../assets/projectlite.gif"),
        isJob: false,
        color: "#d8e2dc",
        link: "https://github.com/choum/projectlite"
      },
      bump: {
        title: "Bumpie",
        content:
          "Bumpie is a project a friend invited me to assist with the front-end development. This uses React.js to build the front-end and AWS for the back-end. This is an application that allows users to track changes to their habits.",
        src: require("../assets/bumpie.png"),
        isJob: false,
        color: "#f4c0b8",
        link: "https://github.com/Vuologist/bumpie/"
      }
    };
  }
};
</script>

<style scoped lang="scss">
@import "../scss/_variable.scss";
.resumeWrapper {
  margin-top: 2em;
}
.color:nth-child(1) {
  background-color: $peachcrayola;
}
.md-card:nth-child(2) .color {
  background-color: $peachcrayola;
}

#overWrapper {
  margin-bottom: 3em;
}

img {
  filter: brightness(70%);
}
</style>
