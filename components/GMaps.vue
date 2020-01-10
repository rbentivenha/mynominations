<template functional>
  <v-row>
    <v-card width="600">
      <iframe
        width="600"
        height="500"
        id="gmap_canvas"
        :src="props.link"
        frameborder="0"
        scrolling="no"
        marginheight="0"
        marginwidth="0"
      ></iframe>
    </v-card>
  </v-row>
</template>

<script>
export default {
  props: {
    link: {
      type: String
    }
  }
};
</script>
