<template>
  <div>
    <nav-header/>
    <ciudad-clima/>
  </div>
</template>

<script>
// @ is an alias to /src
import NavHeader from '@/views/layout/NavHeader.vue'
import CiudadClima from '../components/CiudadClima.vue'

export default {
  name: 'Home',
  components: {
    NavHeader,
    CiudadClima
  }
}
</script>

   