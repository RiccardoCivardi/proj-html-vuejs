<script>

/* Import data */
import teamData from '../../data/partials/teamData';
import {getImagePath} from '../../data/methods'

export default {

  name: 'TeamSection',

  data(){
    return{

      teamData,
      getImagePath

    }
  }

}

</script>

<template>

  <section class="section-wrapper">

    <div class="container-xl">

      <div class="row">
  
        <div class="col-12 col-sm-10 offset-sm-1 col-lg-8 offset-lg-0 ">
          
          <p class="subtitle mb-4">We like what we do</p>
          <h2 class="mb-4"><span>Team</span> of Experts</h2>
          <p class="text mb-4">Ethics and integrity the basis on wich our professionals build their carrers. <br/>They are foundamentals that become daily attitudes.</p>
  
          <div class="row row-cols-1 row-cols-md-2 g-5 pt-3">
  
            <div class="col d-flex" v-for="(member, index) in teamData" :key="index">
              
              <div class="image me-4">
                <img :src="getImagePath(`${member.img}.jpg`)" :alt="member.name">
              </div>
  
              <div class="text d-flex flex-column justify-content-around">
                <h4 class="name">{{member.name}}</h4>
                <p>{{member.role}}</p>

                <div>
                  <a v-for="(social, index) in member.social" :key="index" :href="social.href" class="me-1">
                    <i class="fa-brands" :class="`fa-${social.className}`"></i>
                  </a>
                </div>

              </div>
  
            </div>
  
          </div>
  
        </div>

        <div class="col-12 col-sm-10 offset-sm-1 col-lg-4 offset-lg-0 mt-5 ps-lg-5">
          <div class="card rounded-1">
            <h4 class="mb-4">President Speech</h4>
            <p v-for="(text,index) in teamData[3].speech" :key="index" class="mb-4">{{text}}</p>
            <div class="d-flex justify-content-between align-items-center">
              <span>{{teamData[3].name}}</span>
              <i class="fa-solid fa-quote-right"></i>
            </div>
          </div>
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
 @include section(dark);
 .subtitle {
  @include subtitle(s700);
 }
 h2 {
  @include title(light);
 }
 .text {
  @include paragraph(light);
 }
 .image {
  width: 110px;
  height: 100%;
  border-radius: 5px;
  overflow: hidden;
  img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
  }
 }
 .text{
  h4 {
    @include titleSmall(light);
    margin-bottom: 0;
  }
  p {
    @include paragraph(light);
    text-transform: uppercase;
    font-size: 0.9rem;
  }
  a {
    display: inline-block;
    background-color: $dark-rgba-primary;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    line-height: 40px;
    text-align: center;
  }
 }
 .card{
  background-color: $primary;
  padding: 2rem;
  overflow: auto;
  max-height: 500px;
  h4 {
    @include titleSmall(light);
  }
  p, span {
    @include paragraph(light);
  }
  span {
    text-transform: uppercase;
    font-weight: 700;
    font-size: 0.9rem;
    letter-spacing: 1px;
  }
  i{
    color: rgba(0,0,0,0.3);
    font-size: 2.5rem;
  }
 }
}

</style>