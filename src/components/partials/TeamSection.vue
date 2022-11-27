<script>

/* Import data */
import processManagement from '../../data/partials/processManagement';

/* Import componets: BussinessCard */
import ManagementCard from './ManagementCard.vue';

export default {

  name: 'TeamSection',

  components: {

    ManagementCard

  },

  data(){
    return{

      processManagement

    }
  }

}

</script>

<template>

  <section class="section-wrapper">

    <div class="row container-xl">

      <div class="col-12 col-sm-8 offset-sm-2 col-md-6 offset-md-3 col-lg-8 offset-lg-0">
        
        <p class="subtitle mb-4">We like what we do</p>
        <h2 class="mb-4"><span>Team</span> of Experts</h2>
        <p class="text mb-4">Ethics and integrity the basis on wich our professionals build their carrers. They are foundamentals that become daily attitudes.</p>

        <div class="row row-cols-1 row-cols-md2">

          <div class="col">

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
  @include subtitle(s700);
 }
 h2 {
  @include title(light);
 }
 .text {
  @include paragraph(light);
 }
}

</style>