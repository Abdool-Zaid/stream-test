<template>
  <div>
    <div id="skillsBody">
      <div class="testCard" v-for="skill in skills" :key="skill">
        <div class="skillCard">
          <h2>{{ skill.name }}</h2>
          <p>level:{{ skill.level }}%</p>
          <div
            class="level"
            style="width:50px height:1% background-color"
          ></div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "skills",
  data() {
    return {
      skills: this.$store.state.skills,
    };
  },
  //   computed:{
  //     skills:()=>{
  // return this.$store.state.skills
  //     }
  //   }
};
</script>
<style scoped>
#skillsBody {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-evenly;
  margin: var(--se);
  padding: var(--se);
}
.skillCard {
  /* min-width: 130px; */
  margin: var(--se);
  padding: var(--se);
  color: var(--thirty);
      width: 35vw;
  background-color: var(--sixty);
  /* border: 3px solid var(--acc); */
  box-shadow: 2px 2px 6px #bebebe, -2px -2px 6px var(--acc);
}

/* media Querries */
@media only screen and (max-width: 966px) {
        .skillCard{
          width: 68vw;
        }  
    }
@media only screen and (max-width: 270px) {
  .skillCard {
    font-size: 0.6em;
  }
}
</style>
