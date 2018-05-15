<template>
 <section class="section">
   <div class="hero is-primary">
     <div class="hero-body">
       <div class="container">
         <h1 class="title is-1">Test</h1>
         <h2 class="subtitle">Test for cloudserver</h2>
       </div>
     </div>
   </div>
   <br>
<article class="message is-link">
  <div class="message-header">테스트</div>
  <div class="message-body">메세지</div>
</article>
<div class="columns">
  
  <div class="column">
  <div class="notification is-info">
    <figure class="image is-squre">
      <img src="http://r.ddmcdn.com/w_830/s_f/o_1/cx_20/cy_1463/cw_2528/ch_1422/APL/uploads/2014/11/puppy-cam-veer-2893191.jpg" alt="">
    </figure>
  </div>
  </div>

  <div class="column">
    <div class="notification is-info">
    <div class="message-header is-success">
      <p>오늘의 개 사진</p>
    </div>
    <div class="message-body">
    <figure class="image is-squre">
      <img v-bind:src="image" alt="">
    </figure>
    </div>
    </div>
  </div>

</div>

 </section>
</template>

<script>
  import axios from 'axios';
  export default{
    data(){
      return{}
    },
    async asyncData(){
      const myimage = await axios.get('https://dog.ceo/api/breeds/image/random');
      return{image: myimage.data.message};
    }
  };
</script>
