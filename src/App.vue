<template>
  <router-view/>
</template>

<style>
  *{
    padding: 0;
    margin:0;
    box-sizing: border-box;
    word-wrap: break-word;

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
html{
  width: 100vw;
  height: 100vh;
  position: fixed;
  left:0;
  top: 0;
}
  body{
    overflow-y: hidden;
    background-image: radial-gradient(circle, #664cc5, #ad36b2, #dc1491, #f71069, #ff3e3e);
    background-repeat: no-repeat;
  background-attachment: fixed;
  background-position: center;
  background-size: 100vw 100vh;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color:var(--acc);
}

</style>
