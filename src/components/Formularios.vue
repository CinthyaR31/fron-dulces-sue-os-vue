<template>
  <div class="container" id="Tabla_precios">
    <h2 class="text-center">Tabla de precios</h2>
    <div class="card-deck mb-5" id="cartas_formulario">
      <!-- carta selección tortas-->
      <FormularioTorta/>

      <!-- carta selección cupcakes-->
      <div class="card" id="carta_cupcakes">
        <img src="logos/imagenes formulario/carta cupcakes.png" class="card-img-top" alt="...">
        <div class="card-body">
          <h4 class="card-title text-center">Personaliza tus cupcakes</h4>
          <p class="card-text text-center">Selecciona el sabor de la base del cupcake, escoge un relleno y
            finalmente, selecciona un sabor para la decoración.</p>


          <h5>Selecciona el sabor base</h5>
          <select class="custom-select mb-2">
            <option selected>Selecciona la opción</option>
            <option value="1">Chocolate</option>
            <option value="2">Vainilla</option>
            <option value="3">Marmoleado</option>

          </select>
          <h5>Selecciona el sabor del relleno</h5>
          <select class="custom-select mb-2">
            <option selected>Selecciona la opción</option>
            <option value="1">Ganache de chocolate</option>
            <option value="2">Frutos rojos</option>
            <option value="3">Maracuyá</option>

          </select>
          <h5>Selecciona el color de la decoración</h5>
          <select class="custom-select mb-2">
            <option selected>Selecciona la opción</option>
            <option value="1">Azul</option>
            <option value="2">Rosa</option>
            <option value="3">Blanco crema</option>
            <option value="4">Morado</option>
          </select>

        </div>

        <div class="card-footer">
          <button type="button" class="btn btn-primary btn-lg btn-block">Enviar pedido</button>
        </div>
      </div>

      <!-- carta selección entremet-->
      <div class="card" id="carta_entremet">
        <img src="logos/imagenes formulario/Carta entremet.png" class="card-img-top" alt="...">
        <div class="card-body">
          <h4 class="card-title">Personaliza tu entremet</h4>
          <p class="card-text">Primero, selecciona el sabor del mousse (base). Segundo, selecciona el sabor
            del relleno. Tercero, selecciona el color de la decoración.</p>
          <h5>Selecciona el sabor base</h5>
          <select class="custom-select mb-2">
            <option selected>Selecciona la opción</option>
            <option value="1">Arequipe</option>
            <option value="2">Frutos rojos</option>
            <option value="3">Café</option>
            <option value="4">Chocolate</option>
            <option value="5">Chocolate blanco</option>

          </select>
          <h5>Selecciona el sabor del relleno</h5>
          <select class="custom-select mb-2">
            <option selected>Selecciona la opción</option>
            <option value="1">Guanabana</option>
            <option value="2">Frutos rojos</option>
            <option value="3">Maracuyá</option>
            <option value="4">Mora</option>

          </select>
          <h5>Selecciona el color de la decoración</h5>
          <select class="custom-select mb-2">
            <option selected>Selecciona la opción</option>
            <option value="1">Azul</option>
            <option value="2">Rosa</option>
            <option value="3">Rojo</option>
            <option value="4">Morado</option>
            <option value="5">Negro</option>
          </select>

        </div>
        <div class="card-footer">
          <button type="button" class="btn btn-primary btn-lg btn-block">Enviar pedido</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style>

#cartas_formulario h5 {
  color: #E17E99;
}

#cartas_formulario button {
  background: #E17E99;
  border: transparent;
}


</style>

<script>

import FormularioTorta from './FormularioTorta';

export default {
  name: 'App',
  components: {
    FormularioTorta
  }
}

</script>