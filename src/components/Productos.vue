<template>
  <div class="container" id="Seccion_especialidades">
    <div class="row">
      <div class="col-12 mb-2">
        <h2 class="text-center">Nuestras especialidades</h2>
      </div>
    </div>
    <div class="row">
      <div class="col-md-4 col-xs-12" v-for="producto in productos" :key="producto._id">
        <div class="card-deck">
          <div class="card">
            <img
                v-bind:src="'./logos/' +producto.url_imagen" class="card-img-top" alt="carta torta flores">
            <div class="card-body">
              <h5 class="card-title text-center">{{producto.titulo}}</h5>
              <p class="card-text text-center">{{producto.descripcion}}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style></style>

<script>

import axios from 'axios'

export default {
  data() {
    return {
      productos: null,
    }
  },


// Se invocan al crearse el componente
  mounted() {
    this.getProductos();
  }, methods: {
    getProductos() {
      console.log("Get Banners")
      axios.get('http://localhost:3000/dulces-suenos/productos').then(
          (data) => {
            console.log("data productos> ", data.data);
            this.productos = data.data;
          }
      )
    }

  }
}
</script>