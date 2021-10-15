<template>
  <div id="carousel1" class="carousel slide" data-ride="carousel">


    <div id="carouselExampleCaptions" class="carousel slide" data-ride="carousel">
      <div class="carousel-inner" v-for="(banner, index) in banners" :key="banner._id">
        <div class="carousel-item" :class="{'active': index == 1}">
          <img v-bind:src="'./logos/' +banner.url_imagen" class="d-block w-100" v-bind:alt="banner.titulo">
          <div class="carousel-caption d-none d-md-block">
            <h5>{{ banner.titulo }}</h5>
            <p>{{ banner.descripcion }}</p>
          </div>
        </div>
      </div>
<!--      <a class="carousel-control-prev" href="#carouselExampleCaptions" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="carousel-control-next" href="#carouselExampleCaptions" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>-->
    </div>
  </div>
</template>


<style>

</style>

<script>

import axios from 'axios'

export default {
  data() {
    return {
      banners: null,
    }
  },


// Se invocan al crearse el componente
  mounted() {
    this.getBanners();
  }, methods: {
    getBanners() {
      console.log("Get Banners")
      axios.get('http://localhost:3000/dulces-suenos/banners').then(
          (data) => {
            console.log("data banners> ", data.data);
            this.banners = data.data;
          }
      )
    }

  }
}

</script>