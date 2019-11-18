<template>
  <div class="home">
    <Carousel :movieSlider="sliderData" />
    <MovieList />  <!-- prop :moviePoster="movieData" -->
   
  </div>
</template>

<script>
  import Carousel from '@/components/Carousel.vue'
  import MovieList from '@/components/MoviesList.vue'
  import DataFromApi from '@/dataApi/movies.js'


  export default {
    name: 'home',
    components: {
      Carousel,
      MovieList
    },
    data() {
      return {
        movieData: [],
        sliderData: [],
      }
    },
    created() {

    },
    mounted() {
      this.getDataFromApi()
    },
    methods: {
      getDataFromApi() {
        this.sliderData = DataFromApi.banners
        this.movieData = DataFromApi.movies
      }
    },
  }
</script>