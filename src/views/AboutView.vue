<template>
  <div class="about">
    <h1>This is an about page</h1>
    <video autoplay  controls loop> </video>
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
      document.querySelector('video').srcObject=stream 
      console.log(stream)
    })
  }
}
}
</script>