<template>
  <div>
    <div class="frame">
     
   
    </div><!--frame-->
    <app-footer></app-footer>
  </div>
</template>

<script>

import footer from '../components/footer'

export default {
  name: 'App',
  components: {
  
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
