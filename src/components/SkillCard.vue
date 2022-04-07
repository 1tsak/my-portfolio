<template>
  <div>
    <div class="col-md-3 card container">
        <div class="card-text">
            <p>Vue</p>
        </div>
      <div class="progress">
        <div class="progress-bar bg-c-red" style="width: 25%"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SkillCard",
  props:{
      
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