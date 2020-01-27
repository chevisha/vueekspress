<template>
  <div >
    <h> register</h>
    <br>
    <input type="email" name="email" v-model="email" placeholder="email"/>
        <br>
    <input type="password" name="pass" v-model="pass" placeholder="pass"/>
    <br>
    <button @click="register">register</button>
  </div>
</template>

<script>
import AuthenticationService from '@/services/AuthenticationService'
export default {
  data () {
    return {
     email:"abc",
     pass:"abc"
    }
  },

    methods:
    {
      async register()
      {
       const response= await AuthenticationService.register({email:this.email});
      console.log(response.data);
    }  
    
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
