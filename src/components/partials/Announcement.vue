<script>

/* Import data */
import contacts from '../../data/partials/contacts';

export default {

  name: 'Announcement',

  data(){
    return{

      contacts,

      limitToPrint: 2
      
    }
  }

}

</script>

<template>

  <div class="announcement-wrapper">
    <div class="container-xl">
      <div class="row d-flex justify-content-between">

        <!-- 0pening time -->
        <div class="col-auto d-none d-sm-block">
          <i class="fa-solid me-2" :class="`fa-${contacts.open.className}`"></i>
          <span>{{contacts.open.text}}</span>
        </div>

        <div class="col-4 offset-8 offset-sm-0 col-sm-3 col-lg-5">

          <ul class="d-flex justify-content-between">

            <!-- Company contacts. To also see the location limitToPrint: 3. If print 3 or more, comment span(text)-->
            <li v-for="n in limitToPrint" :key="n">
              <a :href="contacts.contact[n-1].href">
                <i class="fa-solid" :class="`fa-${contacts.contact[n-1].className}`"></i>
                <span class="d-none d-lg-inline ms-2">{{contacts.contact[n-1].text}}</span>
              </a>
            </li>

            <!-- Social network -->
            <li v-for="(social, index) in contacts.social" :key="index">
              <a :href="social.href">
                <i class="fa-brands" :class="`fa-${social.className}`"></i>
              </a>
            </li>

          </ul>

        </div>

      </div>
    </div>
  </div>
  
</template>

<style lang="scss" scoped>

@use '../../style/partials/vars' as *;

.announcement-wrapper {
  background-color: $bg-300;
  color: $grey;
  padding: 0.9rem 0;
  span {
    font-weight: 300;
  }
  a{
   color: $grey;
   &:hover {
    color: $bg-100;
   } 
  }
}

</style>