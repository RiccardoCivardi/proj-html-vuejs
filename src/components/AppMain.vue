<script>

/* Import components: AboutNetwork, BusinessArea, ProcessManagement, TeamSection */
import AboutNetwork from './partials/AboutNetwork.vue';
import BusinessArea from './partials/BusinessArea.vue';
import ProcessManagement from './partials/ProcessManagement.vue';
import TeamSection from './partials/TeamSection.vue';



export default {

  name:'AppMain',

  components: {

    AboutNetwork,
    BusinessArea,
    ProcessManagement,
    TeamSection

  }

}

</script>

<template>

  <main>

    <AboutNetwork/>

    <BusinessArea/>

    <ProcessManagement/>

    <TeamSection/>

  </main>
  
</template>

<style lang="scss" scoped>

</style>