<script>

/* Import data */
import aboutNetwork from '../../data/partials/aboutNetwork';

export default {

  name: 'BusinessArea',

  data(){
    return{

      aboutNetwork

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
            <div class="col-9">
              <p class="mb-4">We are leaders in providing consultancy services with a set of cutting-edge technologies and a team of experienced and renowned professionals.These are some options that you can hire.</p>
            </div>
            <div class="col-6 col-md-3">
              <a href="#" class="button btn btn-primary">See All</a>
            </div>
          </div>

        </div>

        <div class="col-12 col-md-6 pt-5">
          
          <div class="row g-4">

            <div v-for="(feature, index) in aboutNetwork.features" :key="index" class="col-12 col-md-6">
              <div class="mb-3 d-flex align-items-center">
                <i class="fa-solid me-2" :class="`fa-${feature.className}`"></i>
                <h4>{{feature.title}}</h4>
              </div>
              <p>{{feature.text}}</p>
            </div>

          </div>

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
  .button {
   @include button(solid);
  }
  h4{
    font-weight: 700;
    margin-bottom: 0;
  }
  p:not(.subtitle) {
    color: $bg-300;
    font-weight: 300;
    font-size: 1.1rem;
  }
  i {
    font-size: 1.2rem;
    color: $shiny-primary;
  }
}

</style>