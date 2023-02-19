<template>
    <div class="container-fluid p-3 background_footer mt-2">
        <div class="row row-cols-lg-3 row-cols-md-3 row-cols-sm-1 row-cols-1">
            <div class="col">© 2023 - Bryan Carrozzo</div>
            <div class="col d-flex justify-content-center align-content-center align-items-center col_boolean">
                <span><img src="../../assets/logo.png" alt=""></span>
                <p class="m-0"> <a href="https://boolean.careers/" target="_blank">Boolean</a></p>
            </div>
            <div class="col">
                <ul class="d-flex justify-content-center link_wrapper m-0">
                    <li>
                        <font-awesome-icon icon="fa-brands fa-github" /> <a href="https://github.com/Bilobra" target="_blank">GitHub</a> 
                    </li>
                    <li>
                        <font-awesome-icon icon="fa-brands fa-linkedin" /> <a href="https://www.linkedin.com/in/bryan-carrozzo/" target="_blank">LinkedIn</a> 
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterComponent',
}
</script>

<style lang="scss" scoped>
.background_footer {
    background-color: #F1F1F1;
    box-shadow: 0px -2px 20px #ced4da;
}

.row {
    text-align: center;

    span {
        height: 20px;
        aspect-ratio: 1/1;
        display: flex;

        img {
            width: 100%;
        }
    }

    p {
        font-weight: 600;

    }

    .col_boolean {
        gap: 5px;
    }

    a {
        text-decoration: none;
        color: currentColor;
    }

    .link_wrapper {
        gap: 10px;

        li:hover{
            color:#84878b;
            transform: scale(0.97);
        }
    }
}
</style>