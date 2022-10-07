<template>
  <div class="home">
    <Petal></Petal>
    <!-- nav -->
    <div class="fixedButton navLeft d-flex align-items-center justify-content-between flex-column mb-3">
      <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#testimonials" >
        testimonials</button>
        
            <button type="button" class="btn btn-primary " data-bs-toggle="modal" data-bs-target="#skills" >
              skills</button>
              
              <button type="button" class="btn btn-primary " data-bs-toggle="modal" data-bs-target="#resume" >
                resume</button>
              </div>
              <!-- rightnav -->
              <div class="fixedButton navRight d-flex align-items-center  justify-content-between flex-column mb-3">
                <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#projects" >
                  projects</button>
                  
                  <button type="button" class="btn btn-primary " data-bs-toggle="modal" data-bs-target="#about" >
                    about</button>
                    
                    <button type="button" class="btn btn-primary " data-bs-toggle="modal" data-bs-target="#contact" >
                      contact</button>
                    </div>
                    
                    <!-- modals -->
                    

<div class="modal fade" id="testimonials" tabindex="-1" aria-labelledby="testimonialsLabel" aria-hidden="true">
  <div class="modal-dialog modal-dialog-centered ">
    <div class="modal-content">
      <home-button></home-button>

      <div class="modal-body">
<Testimonials></Testimonials>
      </div>
        <home-button></home-button>
    </div>
  </div>
</div>


<div class="modal fade" id="skills" tabindex="-1" aria-labelledby="skillsLabel" aria-hidden="true">
  <div class="modal-dialog modal-dialog-centered ">
    <div class="modal-content ">
      <home-button></home-button>

      <div class="modal-body">
<Skills></Skills>
      </div>
        <home-button></home-button>
    </div>
  </div>
</div>


<div class="modal fade" id="resume" tabindex="-1" aria-labelledby="resumeLabel" aria-hidden="true">
  <div class="modal-dialog modal-dialog-centered ">
    <div class="modal-content ">
      <home-button></home-button>

      <div class="modal-body">
<Resume></Resume>
      </div>
        <home-button></home-button>
    </div>
  </div>
</div>


<div class="modal fade" id="projects" tabindex="-1" aria-labelledby="projectsLabel" aria-hidden="true">
  <div class="modal-dialog modal-dialog-centered ">

    <div class="modal-content ">
      <home-button></home-button>

      <div class="modal-body">
<Projects></Projects>
      </div>
        <home-button></home-button>
    </div>
  </div>
</div>


<div class="modal fade" id="about" tabindex="-1" aria-labelledby="aboutLabel" aria-hidden="true">
  <div class="modal-dialog modal-dialog-centered ">
    <div class="modal-content ">
      <home-button></home-button>

      <div class="modal-body">
<About></About>
      </div>
        <home-button></home-button>
    </div>
  </div>
</div>


<div class="modal fade" id="contact" tabindex="-1" aria-labelledby="contactLabel" aria-hidden="true">
  <div class="modal-dialog modal-dialog-centered ">
    <div class="modal-content ">
      <home-button></home-button>

      <div class="modal-body">
<Contact></Contact>     
</div>
        <home-button></home-button>
    </div>
  </div>
</div>


  </div>

</template>

<script>
import Petal from "@/components/petal.vue";
import Testimonials from "@/components/testimonials.vue";
import Skills from "@/components/skills.vue";
import Resume from "@/components/resume.vue";
import Projects from "@/components/projects.vue";
import About from "../components/about.vue";
import Contact from "@/components/contact.vue";
import HomeButton from '@/components/homeButton.vue';
// @ is an alias to /src

export default {
  name: "HomeView",
  components: {
    Petal,
    Skills,
    Testimonials,
    Resume,
    Projects,
    About,
    Contact,
    HomeButton
},
};
</script>
<style scoped>
  .fixedButton{
    position: fixed;
  }
  .navLeft{
    top:0;
    left:0;
    height: 100vh;
  }
  .navRight{
    top: 0;
    right:0;
    height: 100vh;
  }

  .fixedButton>*{
    margin:var(--ss);
    background-color: var(--glass);
  }
  .modal-content{
    background-color: var(--mute);
    border: 0px;
}
.fade{
  background-color: var(--bubblebg);

}
</style>
