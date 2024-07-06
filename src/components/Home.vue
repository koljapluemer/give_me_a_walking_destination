<script setup>

</script>

<template>
    <div class="card glass m-2">
      <div class="card-body flex gap-2 flex-wrap justify-center">
        <h2 class="card-title text-gray-800">
          Get a random destination in your area.
        </h2>
        <button
          class="btn btn-primary flex-grow flex flex-col btn-primary"
          @click="alert('WIP')"
        >
          Let's Go
        </button>
      </div>
    </div>
</template>

<style>
body {
  background-image: url("@/assets/b1.jpg");
  background-size: cover;
  background-position: bottom;  
}
</style>