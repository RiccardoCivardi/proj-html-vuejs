<script>

/* Import data */
import businessArea from '../../data/partials/businessArea';

/* Import componets: BussinessCard */
import BusinessCard from './BusinessCard.vue'

export default {

  name: 'BusinessArea',

  components: {

    BusinessCard

  },

  data(){
    return{

      businessArea

    }
  }

}

</script>

<template>

  <section class="section-wrapper">
    <div class="container-xl mx-auto">
      <div class="row">

        <div class="col-12">

          <p class="subtitle mb-4">Our business areas</p>
          <h2 class="mb-4">Excellence in <span>Services</span></h2>

          <div class="row">
            <div class="col-12 col-md-9">
              <p class="mb-4">We are leaders in providing consultancy services with a set of cutting-edge technologies and a team of experienced and renowned professionals.These are some options that you can hire.</p>
            </div>
            <div class="col-4 col-md-3 text-md-end">
              <a href="#" class="button btn btn-primary">See All</a>
            </div>
          </div>

        </div>

        <div class="row row-cols-1 g-4 row-cols-md-2 row-cols-lg-3 mx-auto">

          <BusinessCard v-for="(item, index) in businessArea" :key="index" :item="item"/>

        </div>

      </div>
    </div>
  </section>
  
</template>

<style lang="scss" scoped>

/* Import vars */
@use '../../style/partials/vars' as *;
/* Import mixin */
@use '../../style/partials/mixin' as *;

.section-wrapper{
  @include section(light200);
  .subtitle {
    @include subtitle;
  }
  h2{
    @include title(dark);
  }
  
  p{
    @include paragraph(dark);
  }
  .button {
   @include button(solid);
  }
}

</style>