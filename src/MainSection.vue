<template>
    <section class="myheight m-0 p-0">
        <div class="hero">

            <div class="row row-cols-1 row-cols-md-2 row-cols-sm-2 row-cols-lg-2">
                <div class="col d-flex justify-content-center">

                    <div class="wrapper">
                        <img src="./assets/Bra.png" class="img-fluid" alt="io">

                    </div>


                </div>
            </div>

        </div>
    </section>
</template>

<script>
export default {
    name: 'MainSection',
    components: {

    }
}
</script>

<style lang="scss" scoped>
.myheight {
    height: 100vh;

    .hero {
        height: 500px;
        width: 100%;
        background-color: #F1F1F1;
        padding: 70px 25px;
        margin:0 auto;

        .wrapper{
            width:250px;
            height: 250px;
            border-radius: 50%;
            overflow: hidden;
            text-align: center;
            box-shadow: 0px 7px 20px 1px #00000085;

            img{
                width: 80%;
                filter: drop-shadow(8px 8px 10px gray);
                opacity: 0.95;
                // height: 100%;
            }
        }

       

    }
}
</style>