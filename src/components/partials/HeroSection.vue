<script>

export default {

  name: 'HeroSection'

}

</script>

<template>

  <!-- !!!! background-image in small screen???? -->

  <div class="container-xl mx-auto row d-flex align-items-center justify-content-end">

    <div class="col-12 col-sm-10 offset-sm-2 col-md-8 offset-md-4 col-lg-6 offset-lg-6">

      <p>Fusion & acquisitions</p>
      <h1 class="mb-5">Insurance Consulting</h1>

      <form class="row g-3">

        <div class="col-10 col-sm-6 offset-sm-0">
          <input class="form-control" type="text" placeholder="Name">
        </div>

        <div class="col-10 col-sm-6 offset-sm-0">
          <input class="form-control" type="email" placeholder="Email">
        </div>

        <div class="col-10 col-sm-6 offset-sm-0">
          <input class="form-control" type="text" placeholder="Phone">
        </div>

        <div class="col-10 col-sm-6 offset-sm-0">
          <select class="form-select">
            <!-- to customize (v-for) -->
            <option value="">More info</option>
          </select>
        </div>

        <div class="col-12 ">
          <button type="submit" class="btn btn-primary me-3">Get in touch</button>
          <a class="btn btn-outline-primary">Read more</a>
        </div>

      </form>

    </div>

  </div>
  
</template>

<style lang="scss" scoped>

/* Import vars */
@use '../../style/partials/vars' as *;
/* Import mixin */
@use '../../style/partials/mixin' as *;

.container-xl {
  height: $hero-height;
  p {
    @include subtitle(b400)
  }
  h1{
    font-weight: 900;
    color: $bg-300;
    font-size: 80px;
  }
  input, select {
    width: 100%;
    height: 48px;
    background-color: $grey;
    font-size: 1.1rem;
    padding-left: 15px,
  }
  input{
    border: none;
    border-radius: 5px;
    color: $bg-400;
    &::placeholder {
      font-weight: 300;
      letter-spacing: 0.1rem;
    }
  }
  select {
    font-weight: 300;
  }
  button {
    @include button(solid);
  }
  a{
    @include button(outline);
  }
  

}

</style>