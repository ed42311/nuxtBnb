<template>
  <div class="home-container">
    <div v-for="home in homes" :key="home.objectID" class="home">
      <img class="home-image" :src="home.images[0]" style="width: 200px" />
      <br />
      {{ home.title }}
      <br />
      {{ home.location.address }} {{ home.location.city }}
      {{ home.location.state }}
      <br />
      {{ home.title }}
      <br />
      {{ home.guests }} Guests
      <br />
      {{ home.pricePerNight }} / night
    </div>
  </div>
</template>
<script>
import homes from '~/data/homes'

export default {
  data() {
    return {
      homes: homes.slice(0, 3),
    }
  },
}
</script>

<style scoped>
.home-container {
  display: flex;
}
.home {
  padding: 10px;
}
.home-image {
  padding: 10px;
}
</style>
