<template>
    <div class="col-md-2 card container">
        <div class="card-text">
            <p>{{this.skillname}}</p>
        </div>
      <div class="progress">
        <div :class="pClass" :style="pStyle"></div>
      </div>
    </div>
</template>

<script>
export default {
  name: "SkillCard",
  props:['skillname','logo','progress','color'],
  computed:{
    pStyle(){
      return 'width:'+this.progress+'%;'
    },
    pClass(){
      return 'progress-bar '+this.color
    }
  }
};
</script>

<style scoped>
.card{
    box-shadow: 0px 1px 1px 0px #2345;
    padding: 10px;
}
.card-text{
    display: flex;
}
</style>