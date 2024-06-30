<script setup>
</script>

<template>
 <div class="dashboard">
    <h2 class=" subheading text-grey pt-5" >Welcome to our Dashboard!</h2>
    <v-container class="my-3">

        <v-layout class="ml-3" >
           
            <v-btn small flat color="" @click="sortby('Name')" class="mr-3">
                <v-icon icon="fas fa-person" Left Small></v-icon>
                <span class="caption text-caption">By Name</span>
            </v-btn>
            <v-btn small flat color="" @click="sortby('Score')">
                <v-icon icon="fas fa-score" Left Small></v-icon>
                <span class="caption text-capitalize">By Score</span>
            </v-btn>
            
        </v-layout>

        <v-layout row wrap justify-space-around  class="pa-3 flex">
            <v-flex>
                <div class="caption text-grey">School</div>
            </v-flex>
            <v-flex>
                <div class="caption text-grey">Name</div>
            </v-flex>
            <v-flex>
                <div class="caption text-grey">Score</div>
            </v-flex>
            <v-flex>
                <div class="caption text-grey">Status</div>
            </v-flex>
        </v-layout>

<v-card flat  class="pa-3" v-for="person in info" :key='person.Name'>
    <v-layout row wrap justify-space-around  :class="`person ${ person.status }`"  >
        <v-flex xs12 md6 >
            <p>{{ person.school }}</p>
        </v-flex>
        <v-flex xs6 sm4 md2 >
            <div>{{ person.Name }}</div>

        </v-flex>

        <v-flex xs6 sm4 md2 >
            
            <div>{{ person.Score }}</div>
        </v-flex>

        <v-flex xs6 sm4 md2>
         
            <div>{{ person.status }}</div>
        </v-flex>

    </v-layout>
</v-card>
    </v-container>
 </div>
</template>

<script>

export default{
    data(){
        return{
            info:[
              {school: 'GHIS', Name: 'Oni Emmanuel', Score: 20, status:'fail'} , 
              {school: 'FEGO', Name: 'Adebola Glory', Score: 50, status:'pass'} , 
              {school: 'ESSI', Name: 'Sara Tola', Score: 10, status:'fail'} , 
              {school: 'GHIS', Name: 'Peter Durkher', Score: 60, status:'pass'} , 
              {school: 'MGBS', Name: 'Ali Joy', Score: 90, status:'pass'} , 
              {school: 'BNPS', Name: 'Mercy Praise', Score: 30, status:'fail'} ,  
              {school: 'FEGO', Name: 'Precious Jerry', Score: 20, status:'fail'} , 
              {school: 'ESSI', Name: 'Johnson Max', Score: 54, status:'pass'} , 
              {school: 'CCHS', Name: 'Adetomi Ayo', Score: 15, status:'fail'} , 
              {school: 'TTFS', Name: 'Abdul Ruka', Score: 57, status:'pass'} ,
              {school: 'GHIS', Name: 'Alabi Mary', Score: 39, status:'fail'} , 
              {school: 'FEGO', Name: 'Adelowo Peace', Score: 52, status:'pass'} , 
              {school: 'ESS',  Name: 'Pedro Bolu', Score: 61, status:'pass'} , 
              {school: 'GHIS', Name: 'Isaac Walter', Score: 79, status:'pass'} , 
              {school: 'CORS', Name: 'Mark Felix', Score: 63, status:'pass'} , 
              {school: 'CORS', Name: 'Alfred Jerry', Score: 74, status:'pass'} , 
              {school: 'FEGO', Name: 'Anthony Austin', Score: 42, status:'fail'} , 
              {school: 'USSI', Name: 'Duke Davis', Score: 44, status:'fail'} , 
              {school: 'CCHS', Name: 'Lamessa Faruq', Score: 58, status:'pass'} , 
              {school: 'BNPS', Name: 'Yusuff Bola', Score: 77, status:'pass'} , 
            ]
        }
    },

    methods: {
        sortby(prop){
            this.info.sort((a,b)=> a[prop]< b[prop] ? -1 :1)
        }
    }
}
</script>

<style scoped>
.person.pass{
    border-left: 2px solid #3cd1c2;
}

.person.fail{
    border-left: 2px solid red;
}

.person{
display: flex;
justify-content: space-around;
font-size: 10px;
}

.flex{
    display: flex;
    justify-content: space-around;  
}
</style>
