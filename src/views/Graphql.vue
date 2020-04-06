<template>
  <div>
    <div class="frame">
     <app-admin></app-admin>
   
    </div><!--frame-->
    <app-footer></app-footer>
  </div>
</template>

<script>

import footer from '../components/footer'
import admin from '../components/Admin'

export default {
  name: 'App',
  components: {
    'app-admin': admin,
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
