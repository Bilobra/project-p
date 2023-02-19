<template>
    <section class="myheight m-0 p-0">
        <div class="hero">

            <div class="row row-cols-1 row-cols-md-2 row-cols-sm-2 row-cols-lg-2">
                <div class="col d-flex justify-content-center">

                    <div class="wrapper">
                        <img src="./assets/Bra.png" class="img-fluid" alt="io">

                    </div>


                </div>
                <div class="col">
                    <h2>
                        <a id="home"></a>La mia storia in breve:
                    </h2>
                    <p>
                        A Giugno 2022, inizio un corso professionalizzante
                        full-time della durata di 6 mesi (presso Boolean Careers), volto alla formazionedi figure Junior
                        Full Stack Web Developer.
                    </p>
                    <p>
                        Si è trattato di un corso con lezioni teoriche ed esercitazioni pratiche, dove ho affrontato i due
                        ambiti che compongono la conoscenza dello sviluppatore web front-end e lo sviluppo back-end.
                    </p>
                </div>
            </div>

        </div>
        <div
            class="container-fluid d-flex justify-content-center  flex-column align-items-center row rowx-cols-1 row-cols-sm-1 m-auto container_carousel">
            <div class="text-center col pt-5">
                <h2><a id="projects"></a>Ecco alcuni lavori:</h2>
            </div>
            <CarouselComponent @next="next" @prev="prev" class="col">
                <carousel-slide v-for="(slide, index) in slides" :key="slide" :index="index" :visibleSlide="visibleSlide"
                    :direction="direction" class="text-center carousel_slide">
                    <a :href="slide.link" target="_blank"><img class="img-fluid img_carousel" :src="slide.thumb" /></a>
                    <div class="badge_slide">
                        <h4>{{ slide.name }}</h4>
                    </div>
                </carousel-slide>
            </CarouselComponent>
        </div>
    </section>
</template>

<script>
import CarouselComponent from './components/main/CarouselComponent.vue';
import CarouselSlide from './components/main/CarouselSlide.vue';

export default {
    name: 'MainSection',
    components: {
        CarouselComponent,
        CarouselSlide,
    },

    data() {
        return {
            slides: [

                {
                    thumb: require('./assets/biglietto.jpg'),
                    link: 'https://biglietto-treno-bra.netlify.app/',
                    name: 'Biglietto treno'

                },
                {
                    thumb: require('./assets/boolflix.jpg'),
                    link: 'https://vue-boolflix-bra.netlify.app/',
                    name: 'Boolflix'


                },
                {
                    thumb: require('./assets/boolzapp.jpg'),

                    link: 'https://boolzapp-bra-web.netlify.app/',
                    name: 'Bolzapp web'


                },
                {
                    thumb: require('./assets/campominato.jpg'),

                    link: 'https://campominato-grid-bra.netlify.app/',
                    name: 'Campominato game'


                },
                {
                    thumb: require('./assets/comics.jpg'),

                    link: 'https://comic-dc-bra.netlify.app/',
                    name: 'Comic Dc'


                },
                {
                    thumb: require('./assets/playstation.jpg'),

                    link: 'https://sony-playstation-bra.netlify.app/',
                    name: 'Sony web site'


                },
                {
                    thumb: require('./assets/spotify.jpg'),

                    link: 'https://spotify-web-bra.netlify.app/',
                    name: 'Spotify Web'


                },
                {
                    thumb: require('./assets/todo.jpg'),


                    link: 'https://todolist-bra.netlify.app/',
                    name: 'Todo List'


                }

            ],

            visibleSlide: 0,
            direction: 'left'
        }
    },

    computed: {
        slidesLen() {
            return this.slides.length;
        }
    },


    methods: {
        next() {
            if (this.visibleSlide >= this.slidesLen - 1) {
                this.visibleSlide = 0;
            } else {
                this.visibleSlide++;
            }
            this.direction = "left"
        },
        prev() {
            if (this.visibleSlide <= 0) {
                this.visibleSlide = this.slidesLen - 1;
            } else {
                this.visibleSlide--;
            }
            this.direction = "right"

        }
    }
}
</script>

<style lang="scss" scoped>
.myheight {
    // height: 100vh;
    // box-shadow: 1px 1px 20px #ced4da;
    // box-shadow: 0px 7px 20px 1px #00000085;

    .hero {
        min-height: 500px;
        width: 100%;
        background-color: #F1F1F1;
        padding: 70px 25px;
        margin: 0 auto;
        box-shadow: 1px 1px 20px #ced4da;

        .wrapper {
            width: 250px;
            height: 250px;
            border-radius: 50%;
            overflow: hidden;
            text-align: center;
            box-shadow: 0px 7px 20px 1px #00000085;

            img {
                width: 80%;
                filter: drop-shadow(8px 8px 10px gray);
                opacity: 0.95;

                // height: 100%;

            }
        }



    }

    .container_carousel {
        padding-top: 30px;
        padding-bottom: 70px;
    }

    .img_carousel {
        height: 100%;
        width: 80%;
        object-fit: cover;
        box-shadow: 0px 6px 13px 1px #000000a1;
        border-radius: 12px;
    }



    .carousel_slide:hover img {
        cursor: pointer;
        transform: scale(0.98);
        opacity: 0.8;
    }

    .carousel_slide:hover .badge_slide {
        display: block;
        transition: all 400ms;

    }
}

@media screen and (max-width: 400px) {
    .hero .col {
        padding-bottom: 30px;


    }
}

.badge_slide {
    // width: 50px;
    /* height: 50px; */
    background-color: rgba(0, 0, 0, 0.607);
    color: white;
    position: absolute;
    top: 10px;
    left: 100px;
    border-radius: 8px 8px 0px 8px;
    padding: 8px;
    // font-size: 14px;
    display: none;

    h4 {
        font-size: 12px;
    }

}
</style>