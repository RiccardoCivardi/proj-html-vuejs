<script>

export default {

  name: 'HeaderMenu',

  props:{

    menu: Array,
    direction: String,
    link: String,
    callToAction: String

  }

}

</script>

<template>

  <ul :class="{'flex-column': direction === 'vertical'}" class="d-flex align-items-center justify-content-between w-100">

    <!-- Menu -->
    <!-- Home is active for example -->
    <li v-for="(link, index) in menu" :key="index">
      <a :class="{'active': link.isActive}" class="py-1" href="link.href">{{link.text}}</a>
    </li>

    <!-- BTN call to action -->
    <li>
      <a :href="link" class="btn btn-primary py-1">{{callToAction}}</a>
    </li>

  </ul>
  
</template>

<style lang="scss" scoped>

/* Import vars */
@use '../../style/partials/vars' as *;

a {
  color: $bg-300;
  text-transform: uppercase;
  font-size: 1.2rem;
}

a.btn{
  padding: 0.6rem 1.5rem;
  font-size: 1.3rem;
  color: $bg-100;
  text-transform: uppercase;
  background-color: $dark-primary;
  &:hover {
    background-color: $shiny-primary;
  }
}
a.active{
  color: $shiny-primary;
  font-weight: 700;
}

</style>