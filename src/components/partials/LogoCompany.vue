<script>

/* Import data */
import contacts from '../../data/partials/contacts';

export default {

  name: 'LogoCompany',

  props: {

    size: String

  },

  data(){
    return{

      contacts

    }
  }

}

</script>

<template>

  <a :class="{'logo-small': size === 'small', 'logo-big': size === 'big'}" href="#">

    <span v-for="n in contacts.logoCompany.name" :key="n">{{n}}</span>

  </a>
  
</template>

<style lang="scss" scoped>

/* Import vars */
@use '../../style/partials/vars' as *;
/* Import mixin */
@use '../../style/partials/mixin' as *;

.logo-small {
  @include logo(small);
}
.logo-big {
  @include logo(big);
}

</style>