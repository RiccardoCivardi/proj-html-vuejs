<script>

/* Import data */
import newsData from '../../data/partials/newsData';

/* Import componets: NewsCard */
import NewsCard from './NewsCard.vue';

export default {

  name: 'EditorialContent',

  components: {

    NewsCard

  },

  data(){
    return{

      newsData

    }
  }

}

</script>

<template>

  <section class="section-wrapper">
    <div class="container-xl mx-auto">
      <div class="row">

        <div class="col-12 mb-5">

          <p class="subtitle mb-4">Our editorial content</p>
          <h2 class="mb-4">Latest <span>News</span></h2>

          <div class="row">
            <div class="col-12 col-md-9">
              <p class="mb-4">Every week we publish content about what is best in the business world.</p>
            </div>
            <div class="col-4 col-md-3 text-md-end">
              <a href="#" class="button btn btn-primary">See All</a>
            </div>
          </div>

        </div>

      </div>

      <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 pe-0">

        <NewsCard v-for="(item, index) in newsData" :key="index" :item="item"/>

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