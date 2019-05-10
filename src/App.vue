<template>
  <div id="app">
    <!-- <container-component/> -->
    <!-- <gallery-component /> -->
    <form-component></form-component>
  </div>
</template>

<script>
import ContainerComponent from './components/ContainerComponent.vue'
import GalleryComponent from './components/gallery/GalleryComponent.vue'
import FormComponent from './components/inputs/FormComponent.vue'

export default {
  name: 'app',
  components: {
    ContainerComponent,
    GalleryComponent,
    FormComponent
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
