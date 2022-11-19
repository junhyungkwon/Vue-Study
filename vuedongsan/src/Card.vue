<template>
   <div>
    <img :src="onerooms.image" class="room-img" >
   <h4 @click="send">{{onerooms.title}}</h4>

   
     <p> {{onerooms.price}} 만원</p>
   </div>

</template>

<script>



export default {
    name : 'Card',
    
props:{
    onerooms: Object,
},
methods: {
    send() {
       this. $emit('openModal',this.onerooms.id)
    }

    
},
}
</script>

<style>

</style>