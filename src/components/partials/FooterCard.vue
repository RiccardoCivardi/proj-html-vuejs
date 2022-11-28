<script>

export default {

  name: 'FooterCard',

  props: {

    item: Object

  }

}

</script>

<template>

  <div class="col">
    <div class="card p-4 p-lg-4 p-xl-5 h-100">

      <h4 class="mb-4">{{item.title}}</h4>

      <ul>
        <li v-for="(link, index) in item.menu" :key="index" class="mb-2">
          <a :href="link.href">{{link.text}}</a>
        </li>
      </ul>

    </div>
  </div>
  
</template>

<style lang="scss" scoped>

/* Import vars  */
@use '../../style/partials/vars' as *;

/* Import mixin */
@use '../../style/partials/mixin' as *;


.card {
  background-color: $very-dark-gray;
  border: none;
  border-radius: 12px;
  h4 {
    @include titleSmall(light);
  }
  a {
    @include paragraph(light);
    &:hover {
      color: $primary;
    }
    &::before {
      content: '\f054';
      font-weight: bold;
      font-family: 'Font Awesome 6 free';
      margin-right: 10px;
    }
  }
}

</style>