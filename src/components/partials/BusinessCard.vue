<script>

export default {

  name:'BusinessCard',

  props: {

    item: Object

  }

}

</script>

<template>

  <div class="col">
    <div class="card">
      <div class="d-flex justify-content-between mb-4">
        <i class="main-i fa-solid" :class="`fa-${item.className}`"></i>
        <a :href="item.href">
          <i class="link-i fa-solid fa-arrow-right"></i>
        </a>
      </div>
      <h4 class="mb-4">{{item.title}}</h4>
      <p>{{item.text}}</p>
    </div>
  </div>
  
</template>

<style lang="scss" scoped>

/* Import vars */
@use '../../style/partials/vars' as *;
/* Import mixin */
@use '../../style/partials/mixin' as *;

.card {
  @include card(light);
  .main-i {
    font-size: 2.3rem;
    color: $primary;
  }
  .link-i {
    color: $dark-rgba-primary;
    font-size: 1.5rem;
    font-weight: 700;
  }
  h4 {
   @include titleSmall(dark);
  }
  p {
    @include paragraph(dark);
  }
}


</style>