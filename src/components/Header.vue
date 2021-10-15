<template>
  <!-- MENU ENCABEZADO-->

  <nav class="navbar navbar-expand-lg navbar-light  bg-color-menu">
    <a class="navbar-brand" href="#">
      <img src="../../public/logos/logo-dulces-suenos-small.png" alt="" width="200">
    </a>

    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav mr-auto">
        <li class="nav-item"><a class="nav-link" href="#">Inicio</a></li>
        <li class="nav-item"><a class="nav-link" href="#Seccion_especialidades">Especialidades</a></li>
        <li class="nav-item"><a class="nav-link" href="#Creaciones">Creaciones</a></li>
        <li class="nav-item"><a class="nav-link" href="#Tabla_precios">Tabla de precios</a></li>
        <li class="nav-item"><a class="nav-link" href="#footer">Contacto</a></li>
      </ul>
    </div>
  </nav>
</template>

<style>
body{
  font-family: 'Courgette', cursive;
}

.bg-color-menu {
  background-color: #f7ebed !important;
}

.center-items {
  flex-direction: column;
}
</style>