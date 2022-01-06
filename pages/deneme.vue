<template>
  <div>
   <ul>
     <li v-for="c in getC.countCart" :key="c._id">

       {{c.title}}
     </li>

     
   </ul>
  </div>
</template>

<script>
export default {
computed:{
  getUserId(){
    return this.$store.getters.getUser
  },
    getC(){
        return this.$store.getters.getUserCheck.find(item => {
          return item.userId == this.getUserId.userId
        })
    }
}
}
</script>

<style>

</style>