<template>
  <div class="home">
        <Petal></Petal>
        <!-- Button trigger modal -->
<button type="button" class="btn btn-primary fixedButton" data-bs-toggle="modal" data-bs-target="#about" >
  Launch demo modal
</button>

<!-- Modal -->
<div class="modal fade" id="about" tabindex="-1" aria-labelledby="aboutLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h1 class="modal-title fs-5" id="aboutLabel">Modal title</h1>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        ...
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</div>

        <!-- Full screen modal -->

<div class="modal-dialog modal-fullscreen-sm-down">
  ...
</div>

  </div>
</template>

<script>
import Petal from "@/components/petal.vue";
// @ is an alias to /src

export default {
  name: "HomeView",
  components: {
    Petal,
  },
};
</script>
<style scoped>
  .fixedButton{
    position: fixed;
    bottom: 0;
  }
</style>
