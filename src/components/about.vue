<template>
  <div>
    <div id="aboutBody">
      <div id="aboutlanding">
        <iframe
          src="https://www.linkedin.com/embed/feed/update/urn:li:ugcPost:6983873663385128961"
          height="500"
          width="504"
          frameborder="0"
          allowfullscreen=""
          title="Embedded post"
        ></iframe>
      </div>
      <a
        href="src\assets\Abdool_Zaid_Toorabally.pdf"
        download="CV of Abdool Zaid Toorabally"
        ><button>Download Resume</button></a
      >
    </div>
  </div>
</template>
<script>
export default {
  name: "about",
  data() {
    return {
      toggleVideo: false,
    };
  },
 
};
</script>
<style scoped>
#aboutBody {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
#aboutLanding {
  height: var(--height);
  margin: var(--ss);
  padding: var(--ss);
}
video {
  box-shadow: 2px 2px 6px #bebebe, -2px -2px 6px var(--acc);
  border-radius: 20px;
  width: var(--width);
  height: var(--height);
}
</style>
