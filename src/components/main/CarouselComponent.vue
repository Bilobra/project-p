<template>
    <div class="carousel">
        <slot></slot>

        <button @click="next" class="next">Next</button>
        <button @click="prev" class="prev">Prev</button>
    </div>
</template>

<script>
export default {
    name: 'CarouselComponent',
    methods: {
        next() {
            this.$emit('next')
        },
        prev() {
            this.$emit('prev')

        }
    }
}
</script>

<style lang="scss" scoped>
.carousel {
    position: relative;
    width: 80%;
    height: 600px;
    min-height: 200px;
    overflow: hidden;

}

@media screen and (max-width: 400px) {
    .carousel {
        height: 200px;

        button {
            height: 20px;
            width: 30px;
            font-size: 12px;
        }
    }
}

@media screen and (min-width: 576px) {
    .carousel {
        height: 200px;
        width: 500px;
    }
}

@media screen and (min-width: 768px) {
    .carousel {
        height: 350px;
        width: 800px;
    }
}

button {
    position: absolute;
    height: 40px;
    width: 50px;
    top: calc(50% - 20px);
    background-color: rgba(0, 0, 0, 0.8);
    border: none;
    color: white;
    border-radius: 3px;
}

button:focus,
button:hover {
    outline: none;
    cursor: pointer;
}

.next {
    right: 0;
}

.prev {
    left: 0;
}</style>