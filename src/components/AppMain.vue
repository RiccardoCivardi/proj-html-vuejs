<script>

/* Import components: AboutNetwork, BusinessArea */
import AboutNetwork from './partials/AboutNetwork.vue'
import BusinessArea from './partials/BusinessArea.vue'


export default {

  name:'AppMain',

  components: {

    AboutNetwork,
    BusinessArea

  }

}

</script>

<template>

  <main>

    <AboutNetwork/>

    <BusinessArea/>



  </main>
  
</template>

<style lang="scss" scoped>

</style>