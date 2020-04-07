<template>
  <div class="container">
     this is  my first nuxt-app
     {{response}}
  </div>
</template>

<script>

export default {
  name:"index",
  data(){
   return{
    //  response:''
   }
  },
  asyncData ({app}){
    const reponse= app.$axios.get('/').then(res=>{
      return {
        response:res.data
      }
    })
    return reponse
  }
}
</script>

<style>

 
</style>
