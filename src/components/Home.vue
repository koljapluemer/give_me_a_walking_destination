<script setup>
import { ref, watch, computed, onMounted } from "vue";

import "leaflet/dist/leaflet.css";
import { LMap, LTileLayer } from "@vue-leaflet/vue-leaflet";

const zoom = ref(13);
</script>

<template>
  <div class="card glass m-2">
    <div class="card-body flex gap-2 flex-wrap justify-center">
      <h2 class="card-title text-gray-800">
        Get a random destination in your area.
      </h2>
      <div style="height: 600px; width: 800px">
        <l-map ref="map" v-model:zoom="zoom" :center="[47.41322, -1.219482]" :useGlobalLeaflet="false">
          <l-tile-layer
            url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
            layer-type="base"
            name="OpenStreetMap"
          ></l-tile-layer>
        </l-map>
      </div>
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
