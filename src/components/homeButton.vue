<template>
  <div class="homeButton">
    <button type="button" class="btn btn-primary" data-bs-dismiss="modal">
      Home
    </button>
  </div>
</template>

<script>
export default {
  name: "homeButton",
};
</script>

<style scoped>
.btn-primary{
  background-color: var(--mute);
  color:var(--acc);
}
</style>
