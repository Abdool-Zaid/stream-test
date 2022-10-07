<template>
  <h1>Work experience</h1>
  <div id="resumeBody">
    <div class="jobCard" v-for="job in resume" :key="job">
      <h1>{{ job.name }}</h1>
      <h4>{{ job.jobTitle }}</h4>
      <p>{{ job.desc }}</p>
      <p>developed: {{ job.development[0].skill }}</p>
      <p>duration: {{ job.duration }}</p>
      <a :href="job.link" target="blank"></a>
    </div>
  </div>
</template>
<script>
export default {
  name: "resume",
  data() {
    return {
      resume: this.$store.state.resume,
    };
  },
};
</script>
<style scoped>

#resumeBody {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.jobCard {
  margin: var(--se);
  padding: var(--se);
  color: var(--thirty);
  width: 35vw;
  background-color: var(--sixty);
  box-shadow: 2px 2px 6px #bebebe, -2px -2px 6px var(--acc);
}
ul {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}
/* media Querries */
@media only screen and (max-width: 966px) {
        .jobCard{
          width: 68vw;
        }  
    }
@media only screen and (max-width: 460px) {
  .jobCard {
    font-size: small;
  }
}
</style>
