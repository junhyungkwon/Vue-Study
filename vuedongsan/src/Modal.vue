<template>
  <div class="black-bg" v-if="modalopen == true"> 
<div class="white-bg">
   <img :src="onerooms[누른거].image">
  <h4>{{ onerooms[누른거].title }}</h4>
  <p>{{onerooms[누른거].content}}</p>
  <p>{{onerooms[누른거].price}} 원</p>
  <button @click="$emit('modalclose')"> 닫기 </button> 
 <!-- <button @click="modalopen = false"> 닫기 </button>  -->
   </div>
</div>
</template>

<script>
export default {
    name : "Modal",
props: {
    onerooms: Array,
    누른거: Number,
    modalopen: Boolean,
}
}
</script>

<style>

</style>