<template>
    <div class="contain contain--limit">
        <div class="tabsList">
            <span class="tabsList__item active">all</span>
            <span class="tabsList__item">new releases</span>
            <span class="tabsList__item">most popular</span>
            <span class="tabsList__item">trends</span>
            <span class="tabsList__item">recommendations</span>
        </div>
        <section class="contain contain--row">
            <div class="card" v-for="card in 8" :key="card">
                <div class="card__item">
                    <div class="card__poster">
                        <img class="card__img"
                            src="https://images.fineartamerica.com/images/artworkimages/mediumlarge/1/stunning-vibrant-autumn-foggy-sunrise-english-countryside-landsc-matthew-gibson.jpg"
                            alt="">
                    </div>
                    <div class="card__overlay">
                        <div class="card__overlay__title">
                            <span class="taC ttU opBold mb20">avengers infinity war</span>
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
    export default {
        name: 'MovieList'
    }
</script>

<style lang="scss" scoped>

</style>