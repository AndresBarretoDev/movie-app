<template>
    <v-carousel :show-arrows="false" :cycle="true" :interval="6000" height="auto" hide-delimiter-background>
        <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src" .carousel>
            <div class="v-carousel__mask"></div>
            <div class="v-carousel__content">
                <div class="v-carousel__leftCol">
                    <div class="v-carousel__head">
                        <span class="ttU opBold">aquaman</span>
                    </div>
                    <div class="v-carousel__description">
                        <p>Arthur Curry learns that he is the heir of the underwater kingdom of Atlantis. This will
                            become
                            Aquaman, the emperor of Atlantis, committed to defending the entire planet, both on land and
                            in the
                            seas.</p>
                    </div>
                    <div class="v-carousel__cta">
                        <button class="btn btn--watch mr10">
                            watch now
                        </button>
                        <button class="btn btn--more">
                            more info
                        </button>
                    </div>
                </div>

            </div>
        </v-carousel-item>
    </v-carousel>
</template>

<script>
    export default {
        name: 'Carousel',
        components: {

        },
        data() {
            return {

                items: [{
                        src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
                    },
                    {
                        src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
                    },
                    {
                        src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
                    },
                    {
                        src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
                    },
                ],
            }
        },
    }
</script>