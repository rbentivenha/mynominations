<template>
  <v-row>
    <v-col>
      <v-responsive class="overflow-y-auto" max-height="500">
        <div v-for="(poi, index) in pois" :key="index">
          <POICard :poi="poi" :callback="updateMap" />
        </div>
      </v-responsive>
    </v-col>
    <v-col>
      <GMaps :link="mapLink" />
    </v-col>
  </v-row>
  <!-- <img
          src="https://maps.googleapis.com/maps/api/staticmap?center=Brooklyn+Bridge,New+York,NY&zoom=13&size=600x300&maptype=roadmap&markers=color:blue%7Clabel:S%7C40.702147,-74.015794&markers=color:green%7Clabel:G%7C40.711614,-74.012318&markers=color:red%7Clabel:C%7C40.718217,-73.998284&key="
  />-->
</template>

<script>
import GMaps from "~/components/GMaps.vue";
import POICard from "~/components/POICard.vue";

const _pois = require("~/poi.json");

export default {
  components: {
    GMaps,
    POICard
  },

  computed: {
    pois() {
      return require("~/poi.json");
    },
    mapLink() {
      return `https://maps.google.com/maps?q=${this.lat}%2C%20${this.lng}&t=&z=17&ie=UTF8&iwloc=&output=embed`;
    }
  },

  data() {
    return {
      lat: -22.881594,
      lng: -48.445864
    };
  },

  methods: {
    updateMap(lat, lng) {
      this.lat = lng;
      this.lng = lat;
    }
  }
};
</script>
