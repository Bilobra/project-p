<template>
    <nav class="navbar navbar-expand-lg  my_navbar_bg p-3">
        <div class="container-fluid">


            <a class="navbar-brand" href="#">
                <div class="logo_wrapper">
                    <img src="../../assets/Bilobra.png" alt="">

                </div>
            </a>

            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup"
                aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse justify-content-end" id="navbarNavAltMarkup">
                <div class="navbar-nav navbar_collapse">
                    <a class="nav-link" href="#home">Home</a>
                    <a class="nav-link" href="#projects">Projects</a>
                    <a class="nav-link" href="#skills">Skills</a>

                </div>
            </div>
        </div>
    </nav>
</template>


<script>
export default {
    name: 'NavbarComponent',
}
</script>

<style lang="scss" scoped>
.my_navbar_bg {
    background-color: #F1F1F1;
    box-shadow: 1px 1px 20px #ced4da;
    padding-bottom: 50px;
    // position: fixed;
    // top: 0;
    // left: 0;
    // right: 0;
    // z-index: 999;
   
    // height: 120px;


    .navbar_collapse {
        gap: 50px;
    }
}
.logo_wrapper{
    width: 80px;
    height: 90px;
    img{
        height: 100%;
    }
}

.nav-link,
.navbar-brand {
    color: black;
    font-size: 0.9rem;
    padding:0

}
</style>