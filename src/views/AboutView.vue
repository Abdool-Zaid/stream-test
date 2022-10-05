<template>
  <div class="about">
    <div class="container">
  <div class="petal-1"><HelloWorld></HelloWorld></div>
  <div class="petal-2"><HelloWorld></HelloWorld></div>
  <div class="petal-3"><HelloWorld></HelloWorld></div>
  <div class="petal-4"><HelloWorld></HelloWorld></div>
  <div class="petal-5"><HelloWorld></HelloWorld></div>
</div>
    </div>
</template>
<script>
import HelloWorld from '@/components/HelloWorld.vue';

  export default {
    name: "about",
    components: { HelloWorld }
}
</script>
<style scoped>
.container {  display: grid;
  width: 100vw;
  height: 100vh;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr 1fr;
  gap: 0px 0px;
  grid-auto-flow: row;
  grid-template-areas:
    "petal-1 . petal-2"
    ". petal-3 ."
    "petal-4 . petal-5";
}

.petal-1 { grid-area: petal-1; }

.petal-2 { grid-area: petal-2; }

.petal-3 { grid-area: petal-3; }

.petal-4 { grid-area: petal-4; }

.petal-5 { grid-area: petal-5; }

</style>