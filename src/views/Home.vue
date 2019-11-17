<template>
  <div class="home">
    <Carousel/>
    <MovieList/>
  </div>
</template>

<script>
// @ is an alias to /src
import Carousel from '@/components/Carousel.vue'
import MovieList from '@/components/MoviesList.vue'

export default {
  name: 'home',
  components: {
    Carousel,
    MovieList
  }
}
</script>
