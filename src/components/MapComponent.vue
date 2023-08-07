
<template>
  <div id="map"></div>
</template>

<script lang="ts">
import { defineComponent, onMounted } from 'vue';
import mapboxgl from 'mapbox-gl';


export default defineComponent({
  name: 'MapComponent',
  setup() {
    onMounted(() => {
      mapboxgl.accessToken = 'pk.eyJ1IjoibWlsb2FsZGV2YXJhbiIsImEiOiJjbGt5ZThuZzUxa3RxM3NtYXZqMTZ6Y3BlIn0.cy_ytb88EIHgGBXyofi2zQ';
      const map = new mapboxgl.Map({
        container: 'map',
        style: 'mapbox://styles/mapbox/streets-v11',
        center: [-74.5, 40],
        zoom: 9,
      });
    });
  },
});
</script>