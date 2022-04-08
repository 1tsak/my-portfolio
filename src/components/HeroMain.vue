<template>
  <div class="container">
    <img class="my-logo" src="../assets/ak.png" alt="demo" />
    <p class="name-text">Aakash Jha</p>
    <p class="snippet">Web Developer</p>
    <div class="social">
      <img class="social-ic" src="../assets/github-light.svg" alt="" />
      <img class="social-ic" src="../assets/instagram-light.svg" alt="" />
      <img class="social-ic" src="../assets/youtube-light.svg" alt="" />
    </div>
    <div class="row" v-for="skill in skillData" :key="skill">
      <SkillCard :skillname="skill[0]" :progress="skill[2]" :color="skill[3]"/>
    </div>
    
  </div>
</template>

<script>
import SkillCard from './SkillCard.vue'
export default {
  name: "HeroMain",
  components: {
    SkillCard
  },
  props: {},
  data(){
    return{
      skillData:[
            ['Java','logo-path','75','bg-success'],
            ['Php','logo-path','50','bg-info'],
            ['Python','logo-path','75','bg-danger'],
            ['JavaScript','logo-path','75','bg-warning'],
      ]
    }
  }
};
</script>

<style scoped>
.container {
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
}
</style>