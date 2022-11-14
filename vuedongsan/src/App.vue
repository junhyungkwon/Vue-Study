<template>

<div class= "menu">
  <a href ="" a v-for="testcode in menus" :key="testcode"> {{testcode}} </a>
  

   </div>
  

  <div a v-for="(testcode1,i) in products" :key="i"> <h4>{{testcode1}}</h4>
     <p a v-for="testcode2 in price" :key="testcode2"> {{testcode2}} 만원</p>
   </div>
   
   
  
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      price: ['60', '70', '90'],
      menus: ['Home', 'Shop', 'About'],
      products: ['역삼동 원룸', '천호동 원룸', '마포구 원룸'],
      
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
