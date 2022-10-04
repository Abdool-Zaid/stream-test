<template>
  <div class="about">
    <h1>This is an about page</h1>
    <video autoplay src="../assets/about-video.mp4" controls loop> </video>
    <button @click="loadfunc()" >button</button>
    <audio autoplay controls></audio>
  </div>
},
methods:{
  loadfunc(){
    navigator.mediaDevices.getUserMedia({
      video:true, 
      audio:true
    }).then(stream=>{
      document.querySelector('video').srcObject=stream 
      document.querySelector('audio').srcObject=stream
      console.log(stream)
    })
  }
}
}
</script>