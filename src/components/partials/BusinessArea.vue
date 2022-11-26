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
    <div class="container-xl">
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

        <div class="row row-cols-1 g-4 row-cols-md-2 row-cols-lg-3">

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
  padding: 130px 0;
  background-color: $bg-200;
  .subtitle {
    font-weight: 700;
    color: $shiny-primary;
    text-transform: uppercase;
    font-size: 0.9rem;
  }
  h2 {
    color: $bg-300;
    font-weight: 900;
    font-size: 2.8rem;
    & > span {
      color: $primary;
      @include title(dark);
    }
  }
  p{
    font-size: 1.1rem;
    font-weight: 300;
    color: $bg-300;
  }
  .button {
   @include button(solid);
  }
}

</style>