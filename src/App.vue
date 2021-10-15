<template>
  <div>
    <Header/>
    <hr>
    <Banner/>
    <Jumbotron/>
    <Productos/>
  </div>
</template>

<script>

import Header from './components/Header';
import Banner from './components/Banner';
import Jumbotron from './components/Jumbotron';
import Productos from './components/Productos';

export default {
  name: 'App',
  components: {
    Header,
    Banner,
    Jumbotron,
    Productos
  }
}
</script>

<style>

</style>
