<script>

export default {

  name:'ManagementCard',

  props: {

    item: Object

  }

}

</script>

<template>

  <div class="col p-0">
    <div class="card ">
      <p class="circle mb-4"><span>{{item.id}}</span></p>
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
  padding: 1rem;
  text-align: center;
  .circle {
    width: 40px;
    height: 40px;
    line-height: 40px;
    margin: 0 auto;
    font-weight: 700;
    border-radius: 50%;
    background-color: #C5E0DF;
    color: $primary;
    position: relative;
    &::before, &::after {
      content: '';
      display: block;
      width: 200px;
      height: 5px;
      background-color: #C5E0DF;
      position: absolute;
      top: 17px;
      
    }
    &::before {
      left: -200px;
      
    }
    &::after {
      left: 40px;
    }
  }
  h4 {
   @include titleSmall(dark);
  }
  p {
    @include paragraph(dark);
  }

}

</style>