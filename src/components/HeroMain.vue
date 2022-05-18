<template>
  <div class="container flex flex-col">
    <div class="head-info flex justify-center items-center space-x-6">

      <img class="my-logo border-2 h-32 border-slate-500 rounded-full p-1" src="../assets/ak.png" alt="demo" />
      <div class="info-sec flex flex-col items-start">

        <p class="name-text text-2xl mb-0">Aakash Jha</p>
        <p class="snippet text-sm mb-1">Web Developer</p>
        <div class="social flex space-x-2 border-2 py-1 px-2 rounded-lg border-slate-500">
          <img class="social-ic" src="../assets/github-light.svg" alt="" />
          <img class="social-ic" src="../assets/instagram-light.svg" alt="" />
          <img class="social-ic" src="../assets/youtube-light.svg" alt="" />
        </div>
      </div>
    </div>

    <div class="skills-cont flex flex-col" >
      <p class="items-start text-left font-extrabold text-lg">Skills:-</p>
      <div class="row grid grid-cols-2 gap-2">
        <SkillCard
          v-for="skill in skillData"
          :key="skill"
          :skillname="skill[0]"
          :progress="skill[2]"
          :color="skill[3]"
        />
      </div>
    </div>
  </div>
</template>

<script>
import SkillCard from "./SkillCard.vue";
export default {
  name: "HeroMain",
  components: {
    SkillCard,
  },
  props: {},
  data() {
    return {
      skillData: [
        ["Java", "../assets/github-light.svg", "75", "bg-success"],
        ["JavaScript", "logo-path", "75", "bg-warning"],
        ["Python", "logo-path", "75", "bg-success"],
        ["Php", "logo-path", "50", "bg-info"],
        ["C++", "logo-path", "45", "bg-danger"],
        ["JavaScript", "logo-path", "75", "bg-warning"],
        ["Python", "logo-path", "75", "bg-success"],
        ["Php", "logo-path", "50", "bg-info"],
        ["C++", "logo-path", "45", "bg-danger"],
      ],
    };
  },
};
</script>

<style scoped>
/* .container {
  text-align: center;
  margin: auto;
}
.snippet {
  font-size: 0.8rem;
  color: gray;
  margin: 0;
}
.name-text {
  font-size: 1.2rem;
  margin: 1px;
}
.my-logo {
  height: 6rem;
  margin: 10px;
}
.social-ic {
  margin: 5px;
  height: 1.1rem;
}
.social {
  margin: 5px;
  border: 2px solid #123;
  border-radius: 25px;
  display: inline-block;
  padding: 2px 5px 2px 5px;
}
.social-ic:hover {
  cursor: pointer;
  transform: translateY(-4px);
  transition: 0.3s;
} */
</style>