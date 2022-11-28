<script>

/* Import components: LogoCompany, FooterCard */
import LogoCompany from './partials/LogoCompany.vue';
import FooterCard from './partials/FooterCard.vue';

/* Import data */
import contacts from '../data/partials/contacts';
import menus from '../data/partials/menu';

export default {

  name:'AppFooter',

  components: {

    LogoCompany,
    FooterCard

  },

  data(){
    return {

      contacts,
      menus

    }
  }

}

</script>

<template>

  <footer>

    <div class="footer-top">
      <div class="container-xl">

        <div class="row row-cols-1 row-cols-sm-2 row-cols-lg-4 g-5">

          <div class="col">

            <LogoCompany size="big"/>

            <p class="my-4">A functional HTML Template for Corporate & Business.</p>

            <ul class="mb-4">
              <li v-for="(contact, index) in contacts.contact" :key="index" class="mb-3">
                <a :href="contact.href">
                  <i class="fa-solid me-2" :class="`fa-${contact.className}`"></i>
                  <span>{{contact.text}}</span>
                </a>
              </li>
            </ul>

            <a href="#" class="btn btn-outline-primary">Get in touch</a>

          </div>

          <FooterCard v-for="(menu, index) in menus.footer" :key="index" :item="menu"/>

        </div>

      </div>
    </div>

    <div class="footer-bottom py-4">
      <div class="container-xl d-flex justify-content-between flex-wrap">

        <p class="pe-3">Enjoy the low price. We are tracking any intention of piracy.</p>
        <p>
          <i class="fa-regular fa-copyright"></i>
          2020 NEXGEN is Proudly Powered by 
          <span>Codings</span>
        </p>

      </div>
    </div>

  </footer>
  
</template>

<style lang="scss" scoped>

/* Import vars */
@use '../style/partials/vars' as *;

/* Import mixin */
@use '../style/partials/mixin' as *;

.footer-top {
  @include section(dark);
  p, a {
    @include paragraph(light);
  }
  a.btn {
    @include button(outline);
  }
}

.footer-bottom {
  background-color: $bg-500;
  p {
    @include paragraph(light);
    i {
      font-size: 0.9rem;
    }
    span {
      color: $primary;
    }
  }
}

</style>