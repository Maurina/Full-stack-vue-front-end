<template>
  <div>
    <div class="frame">
     
      <app-earth></app-earth>
    </div><!--frame-->
    <app-footer></app-footer>
  </div>
</template>

<script>

import earth from '../components/earth'
import footer from '../components/footer'

export default {
  name: 'App',
  components: {
  
    'app-earth' : earth,
    'app-footer' : footer,
   
  },
  data: () => ({
     
  }),
}
</script>

<style scoped>
.frame{
  padding: 2%;
   background:#000 url(/assets/images/stars.png) repeat top center; 

}

</style>
