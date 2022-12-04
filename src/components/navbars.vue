<template>
    <div>
        <!-- Sidebar Start -->
        <div class="sidebar pe-4 borders pb-3">
            <nav class="navbar bg-white navbar-dark">
                <router-link to="/" class="navbar-brand d-flex align-items-center fw-bold fs-3 pb-3 ps-3" id="tramos_sas">
                    <h2 class="text-warning">TRAMO <span class="text-dark">S.A.S</span></h2>
                </router-link>
                <div class="navbar-nav w-100">
                    <router-link to="/" class="nav-item nav-link   text-dark fw-bold "><i class="bi bi-person-vcard-fill -alt me-2"></i>Conductores</router-link>
                    <router-link to="/solicitudConductores" class="nav-item nav-link   text-dark fw-bold "><i class="bi bi-person-add me-2"></i>Solicitudes</router-link>
                    <router-link to="/datosConductor" class="nav-item nav-link   text-dark fw-bold "><i class="bi bi-clipboard-data me-2"></i>Datos Conductores</router-link>
                    <router-link to="/datosCliente" class="nav-item nav-link   text-dark fw-bold "><i class="bi bi-file-earmark-bar-graph me-2"></i>Datos Clientes</router-link>
                    <router-link to="/historialView" class="nav-item nav-link   text-dark fw-bold "><i class="bi bi-clock-history me-2"></i>Historial</router-link>
                    <router-link to="/pqrsView" class="nav-item nav-link   text-dark fw-bold "><i class="bi bi-person-fill-exclamation me-2"></i>PQRS</router-link>
                    <router-link to="/signIn" class="nav-item nav-link   text-dark fw-bold "><i class="bi bi-box-arrow-left me-2"></i>Cerrar sesión</router-link>

                </div>
            </nav>
        </div>
        <!-- Sidebar End -->
        
        <!-- Content Start -->
        <div class="content">
            <!-- Navbar Start -->
            <nav class="navbar navbar-expand bg-navcolor navbar-dark sticky-top px-4 py-0">
                <button @click="closeNav" class="sidebar-toggler flex-shrink-0">
                    <i class="bi bi-list text-black"></i>
                </button>
                <div class="navbar-nav align-items-center ms-auto">
                    <div class="nav-item dropdown">
                        <a href="#" class="nav-link dropdown-toggle" data-bs-toggle="dropdown">
                            <i class="bi bi-bell me-lg-2 text-black"></i>
                            <span class="d-none d-lg-inline-flex">Notificaciones</span>
                        </a>

                        <div class="dropdown-menu dropdown-menu-end bg-dark border-0 rounded-0 rounded-bottom m-0">
                            <a href="#" class="dropdown-item">
                                <h6 class="fw-normal mb-0">Perfil actualizado</h6>
                                <small>15 minutes ago</small>
                            </a>
                        <hr class="dropdown-divider">
                        <a href="#" class="dropdown-item">
                            <h6 class="fw-normal mb-0">Nuevo usuario agregado</h6>
                            <small>15 minutes ago</small>
                        </a>
                        <hr class="dropdown-divider">
                        <a href="#" class="dropdown-item">
                            <h6 class="fw-normal mb-0">Contraseña cambiada</h6>
                            <small>15 minutes ago</small>
                        </a>
                        <hr class="dropdown-divider">
                        <a href="#" class="dropdown-item text-center">Ver todas las notificaciones</a>
                        </div>
                    </div>
                    <div class="nav-item dropdown">
                        <a href="#" class="nav-link dropdown-toggle" data-bs-toggle="dropdown">
                            <img class="rounded-circle me-lg-2" src="../assets/images/user.jpg" alt="" style="width: 40px; height: 40px;">
                            <span class="d-none d-lg-inline-flex">Carlos Noguera</span>
                        </a>
                        <div class="dropdown-menu dropdown-menu-end bg-dark border-0 rounded-0 rounded-bottom m-0">
                            <router-link to="/perfilView" class="dropdown-item">Mi perfil</router-link>
                            <router-link to="/signIn" class="dropdown-item">Cerrar sesion</router-link>
                            
                       </div>
                    </div>
                </div>
            </nav>
            <!-- Navbar End -->   


            <!-- router - view -->
                <router-view/> 
            <!-- router - view -->
        </div>
    </div>   

</template>

<script>
export default {
    name: 'MenuSuperior'

}

/* const button = document.querySelector("a.sidebar-toggler");
button.addEventListener("click", () => {
  alert("Hello!! Thanks for click me!");
 button.style.width = "250px";
}); */



/* function closeNav() {
  document.getElementsByClassName("sidebar-toggler").style.width = "0";
  document.getElementsByClassName("content").style.marginLeft= "0";
} */


</script>

<style scoped>

div a.router-link-exact-active {
  background: #bec6dff8;
}
#tramos_sas{
    background: white;
}

:root {
    --primary: #232837;
    --secondary: #232837;
    --light: #6C7293;
    --dark: #000000;
    --white: rgb(255, 255, 255);
    --navcolor: #161627;




    --navegador-item: #fff;
    --cornflower-blue: #816bfc;
    --white: #ffffff;
    --fondo:rgba(242, 242, 242, 0.953);
    --blue: #2706fc;
    --brink-pink: #bec6dff8;
    --tulip-tree: #000000;
    --slate-gray: #dddfe293;
    --botticelli: #c8d0e2;
    --manhattan: #f2c19f;
    --jordy-blue: #9abef8;
}

.bg-navcolor{
    background-color:#161627;
}
.back-to-top {
    position: fixed;
    display: none;
    right: 45px;    
    bottom: 45px;
    z-index: 99;
}


/*** Spinner ***/
#spinner {
    opacity: 0;
    visibility: hidden;
    transition: opacity .5s ease-out, visibility 0s linear .5s;
    z-index: 99999;
}

#spinner.show {
    transition: opacity .5s ease-out, visibility 0s linear 0s;
    visibility: visible;
    opacity: 1;
}


/*** Button ***/
.btn {
    transition: .5s;
}

.btn-square {
    width: 38px;
    height: 38px;
}

.btn-sm-square {
    width: 32px;
    height: 32px;
}

.btn-lg-square {
    width: 48px;
    height: 48px;
}

.btn-square,
.btn-sm-square,
.btn-lg-square {
    padding: 0;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    font-weight: normal;
    border-radius: 50px;
}


/*** Layout ***/
.sidebar {
    position: fixed;
    top: 0;
    left: 0;
    bottom: 0;
    width: 300px;
    height: 100vh;
    overflow-y: auto;
    background: #fff;
    transition: 0.5s;
    z-index: 9999;
}

.borders{
 
 padding-right: 20px;
 box-shadow:
      inset 0 -3em 3em rgba(0,0,0,0.1),
            0 0  0 2px rgb(255,255,255),
            0.3em 0.3em 1em rgba(0,0,0,0.3);
}

.content {
    margin-left: 300px;
    min-height: 100vh;
    background: rgb(244, 241, 241);
    transition: 0.5s;
}

@media (min-width: 992px) {
    .sidebar {
        margin-left: 0;
    }

    .sidebar.open {
        margin-left: -300px;  
    }

    .content {
        width: calc(100% - 300px);
    }

    .content.open {
        width: 100%;
        margin-left: 0;
    }
}

@media (max-width: 991.98px) {
    .sidebar {
        margin-left: -300px;
    }

    .sidebar.open {
        margin-left: 0;
        margin-top: 66px;
    }

    .content {
        width: 100%;
        margin-left: 0;
    }
}


/*** Navbar ***/
.sidebar .navbar .navbar-nav .nav-link {
    padding: 7px 20px;
    color: white;
    font-weight: 500;
    border-left: 3px solid white;
    border-radius: 0 30px 30px 0;
    outline: none;
}

.sidebar .navbar .navbar-nav .nav-link:hover,
.sidebar .navbar .navbar-nav .nav-link.active {
    color: black;
    background:#bec6dff8;
    border-color: black;
}

.sidebar .navbar .navbar-nav .nav-link i {
    width: 40px;
    height: 40px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    background:white;
    color: black;
    border-radius: 40px;
}

.sidebar .navbar .navbar-nav .nav-link:hover i,
.sidebar .navbar .navbar-nav .nav-link.active i {
    background: white;
}

.sidebar .navbar .dropdown-toggle::after {
    position: absolute;
    top: 15px;
    right: 15px;
    border: none;
    content: "\f107";
    font-family: "Font Awesome 5 Free";
    font-weight: 900;
    transition: .5s;
}

.sidebar .navbar .dropdown-toggle[aria-expanded=true]::after {
    transform: rotate(-180deg);
}

.sidebar .navbar .dropdown-item {
    padding-left: 25px;
    border-radius: 0 30px 30px 0;
    color: white;
}

.sidebar .navbar .dropdown-item:hover,
.sidebar .navbar .dropdown-item.active {
    background: black;
}

.content .navbar .navbar-nav .nav-link {
    margin-left: 25px;
    padding: 12px 0;
    color: #ffffff;
    outline: none;
}

.content .navbar .navbar-nav .nav-link:hover,
.content .navbar .navbar-nav .nav-link.active {
    color: #ffffff;
}

.content .navbar .sidebar-toggler,
.content .navbar .navbar-nav .nav-link i {
    width: 40px;
    height: 40px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    background: white;
    border-radius: 40px;
}

.content .navbar .dropdown-item {
    color: white;
}

.content .navbar .dropdown-item:hover,
.content .navbar .dropdown-item.active {
    background: black;
}

.content .navbar .dropdown-toggle::after {
    margin-left: 6px;
    vertical-align: middle;
    border: none;
    content: "\f107";
    font-family: "Font Awesome 5 Free";
    font-weight: 900;
    transition: .5s;
}

.content .navbar .dropdown-toggle[aria-expanded=true]::after {
    transform: rotate(-180deg);
}

@media (max-width: 575.98px) {
    .content .navbar .navbar-nav .nav-link {
        margin-left: 15px;
    }
}


/*** Date Picker ***/
.bootstrap-datetimepicker-widget.bottom {
    top: auto !important;
}

.bootstrap-datetimepicker-widget .table * {
    border-bottom-width: 0px;
}

.bootstrap-datetimepicker-widget .table th {
    font-weight: 500;
}

.bootstrap-datetimepicker-widget.dropdown-menu {
    padding: 10px;
    border-radius: 2px;
}

.bootstrap-datetimepicker-widget table td.active,
.bootstrap-datetimepicker-widget table td.active:hover {
    background: #cc1839;
}

.bootstrap-datetimepicker-widget table td.today::before {
    border-bottom-color: #cc1839;
}


/*** Testimonial ***/
.progress .progress-bar {
    width: 0px;
    transition: 2s;
}


/*** Testimonial ***/
.testimonial-carousel .owl-dots {
    margin-top: 24px;
    display: flex;
    align-items: flex-end;
    justify-content: center;
}

.testimonial-carousel .owl-dot {
    position: relative;
    display: inline-block;
    margin: 0 5px;
    width: 15px;
    height: 15px;
    border: 5px solid #cc1839;
    border-radius: 15px;
    transition: .5s;
}

.testimonial-carousel .owl-dot.active {
    background: black;
    border-color: #cc1839;
}

</style>
