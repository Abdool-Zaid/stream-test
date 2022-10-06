<template>
  <router-view/>
</template>

<style>
  *{
    padding: 0;
    margin:0;
    box-sizing: border-box;
  }
  ::-webkit-scrollbar {
    display:none
  }
  :root{
--glass:#ae36b225;
--sixty: #88888800;
  --bg: #2a51be;
  --thirty: #006c8d;
  --acc: #4e0000;
  --ss: 1%;
  --se: 1em;
  --snx: 30vw;
  --height: 80vh;
  --width: 70vw;
  --sny: 40vh;
  --bubblebg:#cfcbcb;
  --mute: #00000000;
  --cursor:#e600ff;
  }

  body{
    overflow: hidden;
    background-image: radial-gradient(circle, #664cc5, #ad36b2, #dc1491, #f71069, #ff3e3e);  }
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color:var(--acc);
}

</style>
