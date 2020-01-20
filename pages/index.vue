<template>
    <v-card
      @click="props.callback(props.poi.lng, props.poi.lat)"
      class="mb-2"
      :color="hover ? 'indigo lighten-1' : 'indigo'"
    >
      <v-card-title> MapHub para os wayspots de Botucatu </v-card-title>
      <iframe width="100%" height="500" src="https://maphub.net/embed/80746?directions=1&geolocation=1&legend=1&panel=1" frameborder="0" allow="geolocation"></iframe>
    </v-card>
</template>

<script>
export default {};
</script>
