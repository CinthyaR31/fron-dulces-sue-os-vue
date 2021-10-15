<template>
  <div class="card" id="carta_tortas">
    <img src="logos/imagenes formulario/carta tortas.png" class="card-img-top" alt="select tortas">
    <div class="card-body">
      <h4 class="card-title text-center">Personaliza tu {{ producto.nombre_producto }}</h4>
      <p class="card-text text-center">Selecciona el sabor de torta que más te guste, después escoge un
        relleno y finalmente, un color para la decoración. </p>
      <h5>Selecciona el sabor base</h5>
      <select class="custom-select mb-2" v-model="producto.sabor_base">
        <option v-bind:value="base" v-for="(base, index) in sabor_base" :key="base + index">{{ base }}
        </option>
      </select>
      <h5>Selecciona el sabor del relleno</h5>
      <select class="custom-select mb-2" v-model="producto.sabor_relleno">
        <option v-bind:value="relleno" v-for="(relleno, index) in sabor_relleno" :key="relleno + index">
          {{ relleno }}
        </option>
      </select>
      <h5>Selecciona el color de la decoración</h5>
      <select class="custom-select mb-2" v-model="producto.color_decoracion">
        <option v-bind:value="decoracion" v-for="(decoracion, index) in color_decoracion" :key="decoracion + index">
          {{ decoracion }}
        </option>
      </select>
      <h1 class="text-center">{{ producto.costo.toLocaleString() }}$</h1>
    </div>
    <div class="card-footer">
      <button type="button"
              @click="enviarPedido()"
              class="btn btn-primary btn-lg btn-block">Enviar pedido
      </button>
    </div>
  </div>
</template>

<style></style>

<script>

import axios from 'axios'

const fecha = new Date();

export default {
  data() {
    return {
      producto: {
        nombre_producto: 'Torta',
        sabor_base: '',
        sabor_relleno: '',
        color_decoracion: '',
        fecha_creacion: fecha.getFullYear() + '-' + (fecha.getMonth() + 1) + '-' + fecha.getDate(),
        costo: 50000
      },
      sabor_base: [
        'Chocolate', 'Vainilla', 'Yogurt griego', 'Marmoleada'
      ],
      sabor_relleno: [
        'Ganache de chocolate', 'Frutos rojos', 'Duraznos y chantilly', 'Maracuyá'
      ],
      color_decoracion: [
        'Azul', 'Rosa', 'Blaco crema', 'Morado'

      ]
    }

  },
  methods: {
    enviarPedido() {
      console.log("data form > ", this.producto)
      if (this.producto.sabor_base === '' ||
          this.producto.sabor_relleno === '' ||
          this.producto.color_decoracion === '') {
        alert('Verifica alguno de los campos por favor');
      } else {
        axios.post('http://localhost:3000/dulces-suenos/pedidos', this.producto).then(
            (data) => {
              console.log("data banners> ", data.data);
              alert('Pedido enviado exitosamente por un valor de: ' + (this.producto.costo.toLocaleString()));
            }
        )
      }
    }
  }
}
</script>