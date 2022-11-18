<template>


<div class="black-bg" v-if="modalopen == true"> 
<div class="white-bg">
  <h4>{{ onerooms[누른거].title }}</h4>
  <p>상세페이지 내용</p>
  <button @click="modalopen = false"> 닫기 </button>
   </div>
</div>

<div class= "menu">
  <a  v-for="testcode in menus" :key="testcode"> {{testcode}} </a>
   </div>
  

  <div v-for="(a,i) in onerooms " :key="i">
    <img :src="a.image" class="room-img" >
    <h4 @click="modalopen = true; 누른거 = i">{{a.title}}</h4>
     <p> {{a.price}} 만원</p>
   </div>

</template>

<script>

import data from './assets/oneroom.js';




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
