<template>
  <v-layout column justify-center align-center>
    <div class="text-center">
      <v-row>
        <v-col>
          <v-responsive class="overflow-y-auto" max-height="400">
            <POICard />
          </v-responsive>
        </v-col>
        <v-col>
          <GMaps />
        </v-col>
      </v-row>
      <!-- <img
          src="https://maps.googleapis.com/maps/api/staticmap?center=Brooklyn+Bridge,New+York,NY&zoom=13&size=600x300&maptype=roadmap&markers=color:blue%7Clabel:S%7C40.702147,-74.015794&markers=color:green%7Clabel:G%7C40.711614,-74.012318&markers=color:red%7Clabel:C%7C40.718217,-73.998284&key="
      />-->
    </div>
  </v-layout>
</template>

<script>
import GMaps from "~/components/GMaps.vue";
import POICard from "~/components/POICard.vue";

const pois = require("~/poi.json");

export default {
  components: {
    GMaps,
    POICard
  }
};
</script>
