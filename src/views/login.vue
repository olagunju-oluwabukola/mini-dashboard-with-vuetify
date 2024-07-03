<template>
    <div flat  class="mt-12 text-center" > 
        <h3 class="pt-4" @submit="login">Login</h3>
       <form action="">
        
      <input type="text" placeholder="exam no" id="number"  v-model="number" required> <br>
      <h6 v-if="number.length <= 5">Incorrect Reg no</h6> 
      <input type="password" placeholder="password" id="password" v-model="form" required> <br>
      <h6 v-if="form.length <= 5">Incorrect Password</h6> <br>
      <p>Forget Passowrd?</p>
      <button>Submit</button>
       </form>
    </div>
</template>
<script>

export default{
    data(){
        return{
          
                number: '',
                form: ''
        }
    },
    methods:{ login(){
        console.log('clicked')

    }
    }
}
</script>
<style scoped>
input{
    border: 1px solid purple;
    border-radius: 10px;
    margin-top: 20px;
    font-size: 10px;
    padding: 5px;
    width: 200px; 
    color: grey;
    outline: none;
}

button{
    background: purple;
    border-radius: 10px;
    color: #fff;
    font-size: 10px;
    width: 70px; 
    padding: 5px;
    margin-top: 8px;
}

p{
    font-size: 8px;
   margin-left: 100px;
    margin-top: 5px;
    text-decoration: underline;
}

h6{
    color: red;
    font-size: 10px;
    margin-right: 100px;
    margin-top: 0px;
    font-weight: 100;
}
</style>

