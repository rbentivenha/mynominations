<template>
  <v-card width=500>
    <row v-html="iframe"></row>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      iframe: "<iframe width='600' height='500' id='gmap_canvas' src='https://maps.google.com/maps?q=-22.339363%2C%20-49.053652&t=&z=17&ie=UTF8&iwloc=&output=embed' frameborder='0' scrolling='no' marginheight='0' marginwidth='0'></iframe>"
    }
  }
}
</script>
