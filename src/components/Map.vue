<template>
  <div class="map">
      <h2>Peta Dengan VueJs dan LeafletJs</h2>
      <div style="height: 600px; width: 100%">
        <l-map :zoom="zoom" :center="center">
          <l-marker :lat-lng="center"></l-marker>
          <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
        </l-map>
      </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      url:'http://{s}.tile.osm.org/{z}/{x}/{y}.png',
      attribution:'&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors',
      zoom: 12,
      center: [-6.93,107.60],
      bounds: null,

    };
  }
}
</script>
