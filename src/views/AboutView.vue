<template>
  <div class="about">
    <h1>This is an about page</h1>
  <div id="mainbg">

    <video autoplay   loop id="video0"></video>
    <video autoplay   loop id="video1"></video>
    <video autoplay   loop id="video2"></video>
    <video autoplay   loop id="video3"></video>
    <video autoplay   loop id="video4"></video>
    <video autoplay   loop id="video5"></video>
    <video autoplay   loop id="video6"></video>
    <video autoplay   loop id="video7"></video>
  </div>
    <audio autoplay ></audio>
  </div>
</template>
<script>

  export default {
  name: 'about',
  
mounted(){
  this.loadfunc()
},
methods:{
  loadfunc(){
    navigator.mediaDevices.getUserMedia({
      video:true, 
    }).then(stream=>{
      document.querySelector('#video0').srcObject=stream 
      document.querySelector('#video1').srcObject=stream 
      document.querySelector('#video2').srcObject=stream 
      document.querySelector('#video3').srcObject=stream 
      document.querySelector('#video4').srcObject=stream 
      document.querySelector('#video5').srcObject=stream 
      document.querySelector('#video6').srcObject=stream 
      document.querySelector('#video7').srcObject=stream 
      // document.querySelector('audio').srcObject=stream 
      // console.log(stream)

navigator.getBattery().then((battery) => {
console.log(100*battery.level)
console.log(battery.dischargingTime+ 'seconds of battery life remaining' ) 
});
    })
  }
}
}
</script>
<style scoped>
  #mainbg{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100vw;
    height: 100vh;
  }
  video{
position: fixed;
opacity:0.3; 
}

#video0{   
  animation:spin 4s linear infinite;
  width: 100vw;
  }
  #video1{   
    animation:antispin 5s linear infinite;
    width: 87vw;
  }
  #video2{   
    animation:spin 6s linear infinite;
    width: 75vw;  
  }
  #video3{   
    animation:antispin 7s linear infinite;
    width:62vw
  }
  #video4{   
    animation:spin 7s linear infinite;
    width: 50vw;
  }
  #video5{   
    animation:antispin 6s linear infinite;
    width: 37vw;
}
#video6{   
  animation:spin 5s linear infinite;
  width: 25vw;
}
#video7{   
  animation:antispin 4s linear infinite;
  width:13vw
}
@keyframes spin { 100% { -webkit-transform: rotate(360deg); transform:rotate(360deg); } }
  @keyframes antispin{ 100% { -webkit-transform: rotate(-360deg); transform:rotate(-360deg); } }

</style>