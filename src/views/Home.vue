<template>
  <div>
    <div class="frame">
     
      <app-cards></app-cards>
    </div><!--frame-->
    <app-footer></app-footer>
  </div>
</template>

<script>

import cards from '../components/cardsGraphqlDisplay'
import footer from '../components/footer'

export default {
  name: 'home',
  components: {
    'app-cards': cards,
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
