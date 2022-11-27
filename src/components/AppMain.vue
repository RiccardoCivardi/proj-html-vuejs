<script>

/* Import components: AboutNetwork, BusinessArea, ProcessManagement */
import AboutNetwork from './partials/AboutNetwork.vue';
import BusinessArea from './partials/BusinessArea.vue';
import ProcessManagement from './partials/ProcessManagement.vue';



export default {

  name:'AppMain',

  components: {

    AboutNetwork,
    BusinessArea,
    ProcessManagement

  }

}

</script>

<template>

  <main>

    <AboutNetwork/>

    <BusinessArea/>

    <ProcessManagement/>

  </main>
  
</template>

<style lang="scss" scoped>

</style>