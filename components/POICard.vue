<template functional>
  <v-hover v-slot:default="{ hover }">
    <v-card
      width="300"
      @click="props.callback(props.poi.lng, props.poi.lat)"
      class="mb-2"
      :color="hover ? 'indigo lighten-1' : 'indigo'"
    >
      <v-card-title>{{props.poi.title}}</v-card-title>
      <v-card-subtitle>{{props.poi.description}}</v-card-subtitle>
    </v-card>
  </v-hover>
</template>

<script>
export default {
  name: "POICard",
  props: {
    title: {
      default: "Titulo"
    },
    poi: {
      type: Object
    },
    callback: {
      type: Function
    }
  }
};
</script>
