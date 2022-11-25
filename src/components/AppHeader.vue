<script>

/* Import data */
import menu from '../data/partials/menu';

/* Import components: Announcement, LogoCompany, HeaderMenu */
import Announcement from './partials/Announcement.vue';
import LogoCompany from './partials/LogoCompany.vue';
import HeaderMenu from './partials/HeaderMenu.vue';

export default {

  name:'AppHeader',

  components: {

    Announcement,
    LogoCompany,
    HeaderMenu

  },

  data(){
    return{

      menu,

      /* customize CTA*/
      link: '#',
      callToAction: 'get in touch'

    }
  }

}

</script>

<template>

  <header>

    <!-- You can add or remove Announcement and you can edit the data in contact.js -->
    <Announcement/>

    <div class="container-xl py-4 d-flex align-items-center justify-content-between">

      <!-- logo size small -->
      <LogoCompany size="big"/>

      <nav class="col-2 col-lg-9 d-flex align-items-center justify-content-end">
        
        <!-- you can change the displayed menu -->
        <HeaderMenu :menu="menu.header" class="d-none d-lg-flex" :link="link" :callToAction="callToAction"/>

        <!-- hamburger menu -->
        <div class="dropdown d-lg-none">

          <i class="hamburger fa-solid fa-bars fs-1" data-bs-toggle="dropdown" aria-expanded="false"></i>

          <div class="dropdown-menu">

            <!-- you can change the displayed menu -->
            <HeaderMenu :menu="menu.header" direction="vertical" :link="link" :callToAction="callToAction"/>
            
          </div>

        </div>

      </nav>
      
    </div>

  </header>
  
</template>

<style lang="scss" scoped>

/* Import vars */
@use '../style/partials/vars' as *;

.dropdown{
  .hamburger {
    cursor: pointer;
    color: $bg-300;
    &:hover{
      color: $dark-grey;
    }
  }
}

</style>