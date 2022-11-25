<script>

/* Import components: Announcement */
import Announcement from './partials/Announcement.vue';

export default {

  name:'AppHeader',

  components: {

    Announcement

  }

}

</script>

<template>

  <header>

    <!-- You can add or remove Announcement and you can edit the data in contact.js -->
    <Announcement/>


  </header>
  
</template>

<style lang="scss" scoped>

</style>