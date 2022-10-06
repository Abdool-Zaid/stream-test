<template >
    <div>
         <div id="aboutBody">
    <div id="aboutlanding">
      <video src="../assets/about.mp4" controls loop id="aboutVideo"></video>
      <button @click="togglePlay()">play</button>
    </div>
       <a href="../assets/Abdool_Zaid_Toorabally.pdf" download><button >Download Resume</button></a>
  </div>
    </div>
</template>
<script>
export default {
      name: "about",
      data() {
        return {
          toggleVideo:false
        }
      },
methods:{
  togglePlay(){
document.querySelector('#aboutVideo').play().then(video=>{
  console.log('playing')
})
  }
}
}
</script>
<style scoped >

#aboutBody {
  display: flex;
  flex-direction: column;
  justify-content: center;
align-items: center;
}
#aboutLanding {
  height: var(--height);
  margin:var(--ss);
  padding:var(--ss);
}
video {
    box-shadow:  2px 2px 6px #bebebe,
             -2px -2px 6px var(--acc);
  border-radius: 20px;
width: var(--width);
  height: var(--height);
}
    
</style>