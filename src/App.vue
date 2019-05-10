<template>
  <div id="app">
    <!-- <container-component/> -->
    <gallery-component />
  </div>
</template>

<script>
import ContainerComponent from './components/ContainerComponent.vue'
import GalleryComponent from './components/gallery/GalleryComponent.vue'

export default {
  name: 'app',
  components: {
    ContainerComponent,
    GalleryComponent
  },
}
</script>

<style>

  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }

</style>
