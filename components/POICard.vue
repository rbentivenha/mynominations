<template functional>
  <v-card width="300">
    <v-card-title>{{props.title}}</v-card-title>
    <v-card-subtitle>{{props.description}}</v-card-subtitle>
  </v-card>
</template>

<script>
export default {
  name: "POICard",
  props: {
    title: {
      default: "Titulo"
    },
    description: {
      default: "Desc"
    }
  }
};
</script>
