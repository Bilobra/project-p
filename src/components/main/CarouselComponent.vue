<template>
    <div class="carousel">
        <slot></slot>

        <button  @click="next" class="next">Next</button>
        <button @click="prev" class="prev">Prev</button>
    </div>
</template>

<script>
export default {
    name: 'CarouselComponent',
    methods:{
        next(){
            this.$emit('next')
        },
        prev(){
            this.$emit('prev')

        }
    }
}
</script>

<style lang="scss" scoped>
.carousel {
    position: relative;
    width: 80%;
    height: 400px;
    overflow: hidden;

}

button {
    position: absolute;
    height: 40px;
    width: 50px;
    top: calc(50% - 20px);
    background-color: rgba(0,0,0,0.8);
    border: none;
    color:white;
}
button:focus, button:hover{
    outline: none;
    cursor: pointer;
}
.next{
    right: 0;
}
.prev{
    left: 0;
}
</style>