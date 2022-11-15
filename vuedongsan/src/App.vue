<template>

<div class= "menu">
  <a href ="" a v-for="testcode in menus" :key="testcode"> {{testcode}} </a>
  

   </div>
  

  <div>
    <h4>{{products[0]}}</h4>
     <p> {{price[0]}} 만원</p>
     <button @click= "increase">허위매물 신고</button>
     <span>신고수: {{신고수}} </span>
   </div>
   
   <div>
    <h4>{{products[1]}}</h4>
     <p> {{price[1]}} 만원</p>
   </div>

   <div>
    <h4>{{products[2]}}</h4>
     <p> {{price[2]}} 만원</p>
   </div>
   
  
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      신고수: 0,
      price: [60, 70, 90],
      menus: ['Home', 'Shop', 'About'],
      products: ['역삼동 원룸', '천호동 원룸', '마포구 원룸'],
      
    }
  },

  methods : {
    increase() {
      this.신고수 += 1;
    }
  },

  components: {
    
  }
}
</script>

<style>
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
</style>
