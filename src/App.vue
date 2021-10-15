<template>
  <div>
    <Header/>
    <hr>
    <Banner/>
    <Jumbotron/>
    <Productos/>
    <hr>
    <GridInstagram/>
    <Formularios/>
    <Footer/>
  </div>
</template>

<script>

import Header from './components/Header';
import Banner from './components/Banner';
import Jumbotron from './components/Jumbotron';
import Productos from './components/Productos';
import GridInstagram from './components/GridInstagram';
import Formularios from './components/Formularios';
import Footer from './components/Footer';

export default {
  name: 'App',
  components: {
    Header,
    Banner,
    Jumbotron,
    Productos,
    GridInstagram,
    Formularios,
    Footer
  }
}
</script>

<style>

</style>
