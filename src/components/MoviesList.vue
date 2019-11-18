<template>
<div class="contain contain--limit">
    <div class="tabsList">
        <span v-for="(entry, index) in filterList" :item="entry" :key="index" @click="filter = entry; active = index;" :class="[entry == filter ? 'tabsList__item active'  :'tabsList__item','']">
            {{ entry }}
        </span>
    </div>
    <!-- <pre>{{moviePoster}}</pre> -->
    <section class="contain contain--row pb50">
        <div class="card" v-for="card in moviePoster" :key="card.id">
            <div class="card__item">
                <div class="card__poster">
                    <img class="card__img" :src="`${publicPath}posters/`+card.poster" :alt="card.alt_attr">
                </div>
                <div class="card__overlay">
                    <div class="card__overlay__title">
                        <span class="taC ttU opBold mb20">{{card.title}}</span>
                    </div>
                    <div class="card__overlay__cta">
                        <button class="btn btn--watch mb15">
                            watch now
                        </button>
                        <button class="btn btn--more">
                            more info
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</div>
</template>

<script>
import DataFromApi from '@/dataApi/movies.js'

export default {

    name: 'MovieList',
    data() {
        return {
            publicPath: process.env.BASE_URL,
            currentCategory: 'all',
            filterList: ["all", " new releases", "  most popular", " trends", "  my favorites", "  recommendations"],
            filter: "all",
            moviePoster: [],
            fetchedMovie: []
        }
    },
    created() {
        this.fetchedMovie = DataFromApi.movies
    },
    mounted() {

    },
    watch: {
        fetchedMovie: function () {
            this.moviePoster = this.fetchedMovie;
        },
        filter: function (value, oldValue) {
            console.log("value-->", value)
            this.moviePoster =
                value != "all" ?
                this.fetchedMovie.filter((item) => item.categories == value) :
                this.fetchedMovie;
        }
    },
    props: [""]
}
</script>

<style lang="scss" scoped>

</style>
