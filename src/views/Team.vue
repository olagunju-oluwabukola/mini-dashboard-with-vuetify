
<script>
export default{
data(){
  return{
    teams:[
        {name: 'Thomas Edward', role:'Language Tutor', image: '../assets/image/tm2.jpg', about: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum in repellat iste mollitia dolor, dicta labore voluptatem architecto repudiandae vitae doloribus nihil animi.'},
        {name: 'Adetola Mercy', role:'History Tutor', image: '../assets/image/tm2.jpg', about: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum in repellat iste mollitia dolor, dicta labore voluptatem architecto repudiandae vitae doloribus nihil animi.'},
        {name: 'Ayomide John', role:'Geography Tutor', image: '../assets/image/avatar2.jpg', about: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum in repellat iste mollitia dolor, dicta labore voluptatem architecto repudiandae vitae doloribus nihil animi.'},
        {name: 'Issac Wonder', role:'Chemistry Tutor', image: '../assets/image/avatar3.jpg', about: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum in repellat iste mollitia dolor, dicta labore voluptatem architecto repudiandae vitae doloribus nihil animi.'},
        {name: 'Fola James', role:'Technology Tutor', image: '../assets/image/avatar5.jpg', about: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum in repellat iste mollitia dolor, dicta labore voluptatem architecto repudiandae vitae doloribus nihil animi.'},
        {name: 'Andrew Felix', role:'Coordinator', image: '../assets/image/tm4.jpg', about: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum in repellat iste mollitia dolor, dicta labore voluptatem architecto repudiandae vitae doloribus nihil animi.'},
      ]
  }
}
}

</script>

<template>
  <div class="container pt-7">
    <v-card v-for="team in teams" :key="team.name"
    max-width="344"
    hover
  >
    <v-card-item>
      <v-card-title class="name">
        <img src="../assets/image/avatar5.jpg"> {{ team.name }}
      </v-card-title>

      <v-card-subtitle class="role">
        {{ team.role }}
      </v-card-subtitle>
    </v-card-item>

    <v-card-text class="about">
      {{ team.about }}
    </v-card-text>
  </v-card>

  </div>
</template>

<style scoped>
.container{
  display: grid;
 grid-template-columns: repeat(auto-fit, minmax(250px,1fr));
 grid-column-gap: 20px;
 grid-row-gap: 15px;
 margin-top: 3em;
}

.about{
  font-size: 10px;
}

.name{
  font-size: 13px;
}

.role{
  font-size: 11px;
}

img{
  border-radius: 50%;
  width: 25px;
  margin-bottom: -5px;
}
</style>

