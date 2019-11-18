<template>
    <v-carousel :show-arrows="false" :cycle="true" :interval="10000" height="auto" hide-delimiter-background>
        <v-carousel-item v-for="(item,i) in movieSlider" :key="i" :src="`${publicPath}banners/`+item.banner" carousel>
            <div class="v-carousel__mask"></div>
            <div class="v-carousel__content">
                <div class="v-carousel__leftCol">
                    <div class="v-carousel__head">
                        <span class="ttU opBold">{{item.title}}</span>
                    </div>
                    <div class="v-carousel__description">
                        <p>{{item.description}}</p>
                    </div>
                    <div class="v-carousel__cta">
                        <button class="btn btn--watch mr10 ">
                            watch now
                        </button>
                        <button class="btn btn--more">
                            more info
                        </button>
                        <!-- <pre>apibanner {{movieSlider}}</pre> -->
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
                publicPath: process.env.BASE_URL
            }
        },
        created() {
            // console.log("host", `${this.publicPath}`)
        },
        props: ['movieSlider']
    }
</script>