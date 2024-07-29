<template>
    <Card>
        <!-- <template #title>Inicio</template> -->
        <template #body>
            <div id="headphoto">
                <img src="https://movies-proxy.vercel.app/ipx/f_webp&s_1220x659/tmdb/xOMo8BRK7PfcJv9JCnx7s5hj0PX.jpg"
                    noselect nopointer>
                <h2>Dune: Parte Dos</h2>
            </div>

            <section id="movieGrid">
                <h2 class="mb-4">Ultimos Estrenos</h2>
                <Grid class="grid" width="128" gapped radius-border shadow>
                    <div class="movie" v-for="(movie, key) in movies" :key radius-border>
                        <img :src="movie.image" alt="">
                        <p>{{ movie.name }}</p>
                    </div>
                </Grid>
            </section>

            <section id="adCarousel" class="mt-4" shadow>
                <Carousel id="carousel-ad" interval="3000" blackArrows="true">
                    <CarouselItem v-for="(ad, key) in ads" :key :active="key === 0" class="carouselItemAd"
                        radius-border>
                        <img :src="ad?.url" radius-border>
                    </CarouselItem>
                </Carousel>
            </section>
        </template>
    </Card>
</template>

<script setup>
import { ref } from 'vue';
import Card from '../../layout/Card.vue';
import { Grid, Carousel, CarouselItem } from "digitalpower";

const ads = ref([
    {
        url: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSinMr3VZrVPOiBn-5bxRynnm4vhsx3iISMGw&s",
    },
    {
        url: "https://storage.googleapis.com/adforum-media/34543684/ad_34543684_169899fa7ed486c5_web.jpg",
    }
]);

const movies = ref([
    {
        image: "https://es.web.img3.acsta.net/pictures/14/11/14/11/16/546987.jpg",
        name: "50 Sombras de gay",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },
    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },

    {
        image: "https://as1.ftcdn.net/v2/jpg/01/34/07/38/1000_F_134073855_zLAqlemgVn3momocAeekziIohiKfrhdg.jpg",
        name: "Test movie",
    },

]);
</script>

<style scoped>
p {
    text-align: left;
}

#headphoto {
    position: absolute;
    top: 0;
    left: 0;

    img {
        width: 100%;
        filter: brightness(.8);
    }

    h2 {
        position: absolute;
        bottom: 0;
        left: 0;
        margin-left: 1em;
        margin-bottom: 1em;
    }
}

#movieGrid {
    margin-top: 55%;
}

.grid {
    background: var(--background-second);
    min-height: 455px;
    max-height: 455px;
    padding: 1.5em 1em;

    overflow-y: auto;
}

.movie {
    width: 128px;
    height: 200px;

    overflow: hidden;

    position: relative;
    background: red;

    cursor: pointer;

    &>img {
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        object-fit: cover;
    }

    &::after {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: black;
        opacity: 0%;

        transition: var(--duration);
    }

    &:hover {
        &::after {
            opacity: 60%;
        }
    }

    &:hover p {
        opacity: 100%;
    }

    p {
        position: absolute;
        top: 50%;
        left: 50%;
        z-index: 10;

        transform: translate(-50%, -50%);
        text-align: center;
        opacity: 0;

        transition: var(--duration);
    }
}

#adCarousel {}

.carouselItemAd {
    width: 100%;
    height: 200px;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
}
</style>