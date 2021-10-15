<template>
  <div class="container" id="Tabla_precios">
    <h2 class="text-center">Tabla de precios</h2>
    <div class="card-deck mb-5" id="cartas_formulario">
      <!-- carta selección tortas-->
      <FormularioTorta/>

      <!-- carta selección cupcakes-->

      <FormularioCupCake/>

      <!-- carta selección entremet-->
      <FormularioEntrement/>
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
import FormularioEntrement from './FormularioEntrement';
import FormularioCupCake from './FormularioCupCake';

export default {
  name: 'App',
  components: {
    FormularioTorta,
    FormularioEntrement,
    FormularioCupCake
  }
}

</script>