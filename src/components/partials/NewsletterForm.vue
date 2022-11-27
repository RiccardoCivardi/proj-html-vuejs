<script>


export default {

  name: 'NewsletterForm',

}

</script>

<template>

  <section class="section-wrapper">

    <div class="container-xl">

      <div class="row">
  
        <div class="col-12 col-lg-6">
          
          <p class="subtitle mb-4">Newsletter</p>
          <h2 class="mb-4"><span>Know</span> First</h2>
          <p class="text mb-4">Follow closely and receive content about our company and the news of the current market</p>
  
        </div>

        <div class="col-12 col-lg-6">

          <form>
            <input type="text" class="form-control w-75 mb-3" placeholder="Name">
            <input type="email" class="form-control w-75 mb-3" placeholder="Email">
            <button type="submit" class="btn btn-primary">Subscribe</button>
          </form>

        </div>
  
      </div>

    </div>
    
  </section>
  
</template>

<style lang="scss" scoped>

/* Import mixin */
@use '../../style/partials/mixin' as *;

.section-wrapper{
  @include section(dark);
  background-image: url('../../assets/img/bg-1.jpg');
  background-size: 140%;
  background-position: center;
    
  .subtitle {
    @include subtitle(s700);
  }
  h2 {
    @include title(light);
  }
  .text {
    @include paragraph(light);
  }
  input{
    @include input();
    background-color: rgba(255,255,255,0.5)
  }
  button {
    @include button(solid);
  }
}

@media screen and (max-width: 820px){
    .section-wrapper {
      background-size: cover;
      background-repeat: no-repeat;
      background-position: right;
    }
  }

</style>