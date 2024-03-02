<template>
    <nav class="navbar shadow px-2 py-0 navbar-light bg-light navbar-expand-lg">
        <a href="#" target="_self" class="navbar-brand order-0 nuxt-link-active">
            <img height="60" src="../assets/img/logo-blue.png">
        </a>
        <div id="nav-collapse" class="order-4 order-md-1 navbar-collapse collapse justify-content-end"
            style="display:none;">
            <ul class="navbar-nav ml-md-auto align-items-md-center">
                <div class="d-md-flex pl-3 p-md-none">
                    <li class="nav-item mr-md-2 text-truncate">
                        <a href="#" class="nav-link active nuxt-link-active">
                            <span id="no">Empleos</span>
                        </a>
                    </li>
                    <li class="nav-item mr-md-2 text-truncate">
                        <a href="#" class="nav-link active nuxt-link-active">
                            <span>Bootcam</span>
                        </a>
                    </li>
                    <li class="nav-item mr-md-2 text-truncate">
                        <a href="#" class="nav-link active nuxt-link-active">
                            <span>Sobre nosotros</span>
                        </a>
                    </li>
                    <li class="nav-item mr-md-2 text-truncate">
                        <a href="#" class="nav-link active nuxt-link-active">
                            <span>Para profesionales</span>
                        </a>
                    </li>
                    <li class="nav-item mr-md-2 text-truncate">
                        <a href="#" class="nav-link active nuxt-link-active">
                            <span>Para empresas</span>
                        </a>
                    </li>
                </div>
            </ul>
        </div>
    </nav>
</template>

<style>
span {
    font-size: 16px !important;
    font-family: 'Montserrat', 'Roboto', 'sans-serif' !important;
    color: #00000080 !important;
    font-weight: 500 !important;
}

span:hover {
    color: #000000 !important;
}

span#no {
    font-size: 16px !important;
    font-family: 'Montserrat', 'Roboto', 'sans-serif' !important;
    color: #000000 !important;
}
span#no:hover {
    color: #00000080 !important;
}
</style>