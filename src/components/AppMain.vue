<script>

/* Import components: AboutNetwork, BusinessArea, ProcessManagement, TeamSection, NewsletterForm */
import AboutNetwork from './partials/AboutNetwork.vue';
import BusinessArea from './partials/BusinessArea.vue';
import ProcessManagement from './partials/ProcessManagement.vue';
import TeamSection from './partials/TeamSection.vue';
import EditorialContent from './partials/EditorialContent.vue';
import NewsletterForm from './partials/NewsletterForm.vue'

export default {

  name:'AppMain',

  components: {

    AboutNetwork,
    BusinessArea,
    ProcessManagement,
    TeamSection,
    EditorialContent,
    NewsletterForm

  }

}

</script>

<template>

  <main>

    <AboutNetwork/>

    <BusinessArea/>

    <ProcessManagement/>

    <TeamSection/>

    <EditorialContent/>

    <NewsletterForm/>

  </main>
  
</template>

<style lang="scss" scoped>

</style>