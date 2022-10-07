<template>
  <div class="petal">
    <div class="container">
      <div class="petal-1">
        <div class="mainbg">
    <video autoplay loop class="video0"></video>
    <video autoplay loop class="video1"></video>
    <video autoplay loop class="video2"></video>
    <video autoplay loop class="video3"></video>
    <video autoplay loop class="video4"></video>
    <video autoplay loop class="video5"></video>
    <video autoplay loop class="video6"></video>
    <video autoplay loop class="video7"></video>
  </div>
      </div>
      <div class="petal-2">
        <div class="mainbg">
    <video autoplay loop class="video7"></video>
    <video autoplay loop class="video6"></video>
    <video autoplay loop class="video5"></video>
    <video autoplay loop class="video4"></video>
    <video autoplay loop class="video3"></video>
    <video autoplay loop class="video2"></video>
    <video autoplay loop class="video1"></video>
    <video autoplay loop class="video0"></video>
  </div>
      </div>
      <div class="petal-3">
        <div class="mainbg">
    <video autoplay loop class="video0"></video>
    <video autoplay loop class="video1"></video>
    <video autoplay loop class="video2"></video>
    <video autoplay loop class="video3"></video>
    <video autoplay loop class="video4"></video>
    <video autoplay loop class="video5"></video>
    <video autoplay loop class="video6"></video>
    <video autoplay loop class="video7"></video>
  </div>
      </div>
      <div class="petal-4">
        <div class="mainbg">
    <video autoplay loop class="video7"></video>
    <video autoplay loop class="video6"></video>
    <video autoplay loop class="video5"></video>
    <video autoplay loop class="video4"></video>
    <video autoplay loop class="video3"></video>
    <video autoplay loop class="video2"></video>
    <video autoplay loop class="video1"></video>
    <video autoplay loop class="video0"></video>
  </div>
      </div>
      <div class="petal-5">
        <div class="mainbg">
    <video autoplay loop class="video0"></video>
    <video autoplay loop class="video1"></video>
    <video autoplay loop class="video2"></video>
    <video autoplay loop class="video3"></video>
    <video autoplay loop class="video4"></video>
    <video autoplay loop class="video5"></video>
    <video autoplay loop class="video6"></video>
    <video autoplay loop class="video7"></video>
  </div>
      </div>
    </div>
    
    <audio autoplay ></audio>
  </div>
</template>
<script>

  export default {
  name: 'petal',
  data() {
    return {
      perms:'granted'
    }
  },
mounted(){
  this.loadfunc()
},
methods:{
  loadfunc(){
    // console.log(navigator.mediaDevices.getUserMedia({video:true}).then(stream=>{stream.perms}))
    navigator.mediaDevices.getUserMedia({
      video:true, 
    }).then(stream=>{
      document.querySelectorAll('.video0').forEach((leaf=>{
        leaf.srcObject=stream 
      }))
      document.querySelectorAll('.video1').forEach((leaf=>{
        leaf.srcObject=stream 
      }))
      document.querySelectorAll('.video2').forEach((leaf=>{
        leaf.srcObject=stream 
      }))
      document.querySelectorAll('.video3').forEach((leaf=>{
        leaf.srcObject=stream 
      }))
      document.querySelectorAll('.video4').forEach((leaf=>{
        leaf.srcObject=stream 
      }))
      document.querySelectorAll('.video5').forEach((leaf=>{
        leaf.srcObject=stream 
      }))
      document.querySelectorAll('.video6').forEach((leaf=>{
        leaf.srcObject=stream 
      }))
      document.querySelectorAll('.video7').forEach((leaf=>{
        leaf.srcObject=stream 
      }))
      // document.querySelector('audio').srcObject=stream 
      // console.log(stream)

// navigator.getBattery().then((battery) => {
// console.log(100*battery.level)
// console.log(battery.dischargingTime+ 'seconds of battery life remaining' ) 
// });


// navigator.permissions.query({name: 'camera'})
//  .then((permissionObj) => {
//   console.log(permissionObj);
//  })
    })
  }
}
}
</script>
<style scoped>
  .mainbg{
    display: flex;
    justify-content: center;
    align-items: center;
  }
  video{
    position: fixed;
    opacity:0.3; 
    border-radius: 50%;
  }

  .video0{   
    animation:spin 4s ease infinite;
    transform-origin:center; 
    width: 100%;
  }
  .video1{   
    animation:antispin 5s ease infinite;
    transform-origin:center; 
    width: 87%;
  }
  .video2{   
    animation:spin 6s ease infinite;
    transform-origin:center; 
    width: 75%;  
  }
  .video3{   
    animation:antispin 7s ease infinite;
    transform-origin:center; 
    width:62%;
  }
  .video4{   
    animation:spin 7s ease infinite;
    transform-origin:center; 
    width: 50%;
  }
  .video5{   
    animation:antispin 6s ease infinite;
    transform-origin:center; 
    width: 37%;
  }
  .video6{   
    animation:spin 5s ease infinite;
    transform-origin:center; 
    width: 25%;
  }
  .video7{   
  animation:antispin 4s ease infinite;
  transform-origin:center; 
  width:13%;
}
.container {  display: grid;
  width: 100vw;
  height: 100vh;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr 1fr;
  gap: 0px 0px;
  animation:spin 4s ease infinite;
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

@keyframes spin { 100% { -webkit-transform: rotate(360deg); transform:rotate(360deg); } }
@keyframes antispin{ 100% { -webkit-transform: rotate(-360deg); transform:rotate(-360deg); } }

</style>