<script>

/* Import data */
import processManagement from '../../data/partials/processManagement';

/* Import componets: BussinessCard */
import ManagementCard from './ManagementCard.vue';

export default {

  name: 'ProcessManagement',

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
    <div class="container-custom mx-auto text-center px-2">
      
      <p class="subtitle mb-4">How it works in practice</p>
      <h2 class="mb-4"><span>Process</span> Management</h2>
      <p class="mb-4">We work with innovative methodologies to ensure that the entire reformatting process is done from start to finish as planned.</p>

    </div>

    <div class="container-fluid">
      <div class="container-xxl">

        <div class="row row-cols-1 g-4 row-cols-sm-2 row-cols-md-3 row-cols-lg-5 ">

          <ManagementCard v-for="(item, index) in processManagement" :key="index" :item="item"/>

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
 @include section(light100);
 .container-custom {
  max-width: 700px;
  .subtitle {
    @include subtitle;
  }
  h2{
    @include title(dark);
  }
  
  p{
    @include paragraph(dark);
  }
 }
  
}

</style>