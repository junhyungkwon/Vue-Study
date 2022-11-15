<template>


<div class="black-bg" v-if="modalopen == true"> 
<div class="white-bg">
  <h4>상세페이지</h4>
  <p>상세페이지 내용</p>
  <button @click="modalopen = false"> 닫기 </button>
   </div>
</div>

<div class= "menu">
  <a  a v-for="testcode in menus" :key="testcode"> {{testcode}} </a>
  

   </div>
  

  <div>
    <img src="./assets/room0.jpg" class="room-img" >
    <h4>{{products[0]}}</h4>
     <p> {{price[0]}} 만원</p>
     <button @click= "신고수[0]++">허위매물 신고</button>
     <span>신고수: {{신고수[0]}} </span>
   </div>
   
   <div>
    <img src="./assets/room1.jpg" class="room-img">
    <h4>{{products[1]}}</h4>
     <p> {{price[1]}} 만원</p>
     <button @click= "신고수[1]++">허위매물 신고</button>
     <span>신고수: {{신고수[1]}} </span>
   </div>

   <div>
    <img src="./assets/room2.jpg" class="room-img" >
    <h4>{{products[2]}}</h4>
     <p> {{price[2]}} 만원</p>
     <button @click= "신고수[2]++">허위매물 신고</button>
     <span>신고수: {{신고수[2]}} </span>
   </div>
   
  
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      modalopen: true,
      신고수: [0,0,0],
      price: [60, 70, 90],
      menus: ['Home', 'Shop', 'About'],
      products: ['역삼동 원룸', '천호동 원룸', '마포구 원룸'],
      
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
