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

  <div v-if="size === 'small'" class="logo-small">

    <span v-for="n in contacts.nameCompany" :key="n">{{n}}</span>

  </div>

  <div v-else-if="size === 'big'" class="logo-big">

    <span v-for="n in contacts.nameCompany" :key="n">{{n}}</span>

  </div>
  
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