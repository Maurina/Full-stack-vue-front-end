<template>
  <div>
    <div class="frame">
     
    <app-cardEdit></app-cardEdit>
    </div><!--frame-->
    <app-footer></app-footer>
  </div>
</template>

<script>

import footer from '../components/footer'
import cardEdit from '../components/cardEdit'

export default {
  name: 'App',
  components: {
    'app-cardEdit' : cardEdit,
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
