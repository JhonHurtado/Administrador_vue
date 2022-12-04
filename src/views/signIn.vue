<template>

  <div>
    <div class="container-fluid position-relative d-flex p-0">
    <!-- Iniciar Sesión Start -->
    <div class="container-fluid">
        <div class="row h-100 align-items-center justify-content-center" style="min-height: 100vh;"
            id="fondo_inicio_sesion_administrador">
            <div class="col-12 col-sm-8 col-md-6 col-lg-5 col-xl-4">
                <div class="rounded p-4 p-sm-5 my-4 mx-3 border" id="contenedor_inicio">
                    <div class="d-flex align-items-center justify-content-between mb-4">
                        <a class="navbar-brand d-flex align-items-center fw-bold fs-3" href="index.html"
                            id="tramos_sas">
                            <h2 class="text-warning">TRAMO</h2>
                            <h2 class="text-dark">S.A.S</h2>
                            
                        </a>
                    </div>
                    <form class="row g-3 needs-validation" novalidate autocomplete="off">
                        <div class="form-floating mb-3">
                            <input type="email" class="form-control" id="floatingInput" placeholder="name@example.com"
                                required>
                            <label for="floatingInput">Correo Electronico</label>
                            <div class="valid-feedback">
                                Se ve bien!
                            </div>
                            <div class="invalid-feedback">
                                Porfavor ingresa el correo Electronico.
                            </div>
                        </div>
                        <div class="form-floating mb-3">
                            <input type="password" class="form-control" id="floatingPassword" placeholder="Contraseña"
                                required>
                            <label for="floatingPassword">Contraseña</label>
                            <div class="valid-feedback">
                                Se ve bien!
                            </div>
                            <div class="invalid-feedback">
                                Porfavor ingresa la contraseña.
                            </div>
                        </div>
                        <div class="col-12">
                            <button type="submit" class="btn bg-navcolor text-white py-3 w-100 mb-3">Iniciar
                                Sesión</button>
                            <p class="text-center mb-0">Administrador TRAMO</p>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
    <!-- Iniciar Sesión End -->
    </div>

  </div>

</template>
  
  <script>
  export default {
  
  }
  </script>
  
  <style>
  
  </style>