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

  <section class="section-wrapper">
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
                <h4 class="mb-0">{{feature.title}}</h4>
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
  @include section(dark);
  .subtitle {
    @include subtitle;
  }
  h2{
    @include title(light);
  }
  h4{
    @include titleSmall(light);
  }
  p:not(.subtitle) {
    @include paragraph(light);
  }
  i {
    font-size: 1.2rem;
    color: $shiny-primary;
  }
}

</style>