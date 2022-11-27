<script>

/* Import getImagePath */
import {getImagePath} from '../../data/methods';

export default {

  name: 'NewsCard',

  props: {

    item: Object

  },

  data(){
    return{

      getImagePath

    }
  }

}

</script>

<template>

  <div class="col mb-4">
    
    <div class="card">
      
      <img :src="getImagePath(`${item.img}.jpg`)" alt="news picture">
  
      <div class="overlay p-1 p-md-2 p-lg-3 p-xl-5 d-flex flex-column-reverse">
  
        <h4>{{item.title}}</h4>
  
      </div>
  
    </div>

  </div>

  
</template>

<style lang="scss" scoped>

/* Import mixin */
@use '../../style/partials/mixin' as *;

.card{
  border: none;
  border-radius: 10px;
  overflow: hidden;
  position: relative;
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    opacity: 0.9;
  }
  .overlay {
    width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,0.4);
    position: absolute;
    top:0;
    text-align: center;
    h4 {
      @include titleSmall(light);
    }
  }

}



</style>