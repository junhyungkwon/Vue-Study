<template>


<Modal  @modalclose="modalopen = false" :onerooms="onerooms" :누른거="누른거" :modalopen="modalopen"  />

<div class= "menu">
  <a  v-for="testcode in menus" :key="testcode"> {{testcode}} </a>
   </div>
  
  <Discount/>

  <Card @openModal="modalopen = true; 누른거 = $event"   :onerooms="onerooms[i]" v-for="(원룸,i) in onerooms" :key="원룸"/>
  



  <!-- <div v-for="(a,i) in onerooms " :key="i">
    <img :src="a.image" class="room-img" >
    <h4 @click="modalopen = true; 누른거 = i">{{a.title}}</h4> 
     <p> {{a.price}} 만원</p>
   </div> -->

</template>

<script>

import data from './assets/oneroom.js';
import Discount from './Discount.vue';
import Modal from './Modal.vue';
import Card from './Card.vue';




export default {
  name: 'App',
  data() {
    return {
      누른거: 0,
      onerooms: data,
      modalopen: false,
      신고수: [0,0,0],
      menus: ['Home', 'Shop', 'About'],
      
    }
  },

  methods: {
    increase() {
      this.신고수 += 1;
    }
    
  },

  components: {
    Discount : Discount,
    Modal : Modal,
    Card : Card,
    
  }
}
</script>

<style>
body {
  margin : 0;
}
div {
  box-sizing: border-box;
}
.black-bg {
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.5);
  position: fixed; padding: 20px;
}
.white-bg {
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20px;
}


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
  
}
.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a{
  color: white;
  padding: 15px;
}
.room-img{
  width: 100%;
  margin-top: 40px;
}

</style>
