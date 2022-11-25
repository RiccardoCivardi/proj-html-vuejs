<script>

/* Import components: Announcement, LogoCompany */
import Announcement from './partials/Announcement.vue';
import LogoCompany from './partials/LogoCompany.vue';

export default {

  name:'AppHeader',

  components: {

    Announcement,
    LogoCompany

  }

}

</script>

<template>

  <header>

    <!-- You can add or remove Announcement and you can edit the data in contact.js -->
    <Announcement/>

    <div>

      <LogoCompany size="small"/>

    </div>


  </header>
  
</template>

<style lang="scss" scoped>

</style>