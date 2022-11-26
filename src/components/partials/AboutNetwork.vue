<script>

/* Import data */
import aboutNetwork from '../../data/partials/aboutNetwork';

export default {

  name: 'AboutNetwork',

  data(){
    return{

      aboutNetwork

    }
  }

}

</script>

<template>

  <div class="section-wrapper">
    <div class="container-xl">
      <div class="row">

        <div class="col-12 col-md-6">

          <p class="subtitle mb-3">About the network</p>
          <h2 class="mb-3"><span>The</span> Company</h2>

          <p class="mb-3">{{aboutNetwork.text1}}</p>
          <p class="mb-3">{{aboutNetwork.text2}}</p>

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
  </div>
  
</template>

<style lang="scss" scoped>

/* Import vars */
@use '../../style/partials/vars' as *;
/* Import mixin */
@use '../../style/partials/mixin' as *;

.section-wrapper{
  padding: 130px 0;
  background-color: $bg-400;
  .subtitle {
    font-weight: 700;
    color: $shiny-primary;
    text-transform: uppercase;
    font-size: 0.9rem;
  }
  h2, h4 {
    color: $bg-100;
  }
  h2{
    font-weight: 900;
    font-size: 2.8rem;
    & > span {
      @include title(dark);
    }
  }
  h4{
    font-weight: 700;
    margin-bottom: 0;
  }
  p:not(.subtitle) {
    color: $grey;
    font-weight: 300;
    font-size: 1.1rem;
  }
  i {
    font-size: 1.2rem;
    color: $shiny-primary;
  }
}

</style>