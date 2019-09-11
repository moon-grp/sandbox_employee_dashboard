<template>
    <div>

         <v-card
    height="auto"
    class="mx-auto cardbg"
    
  >
   <v-row class="pa-9">
    <v-avatar
    size="100"
    >
      <img
        src="https://cdn.vuetifyjs.com/images/john.jpg"
        alt="John"
      >
    </v-avatar>
    <v-col>
    <h3>Sales Presentation - Live Group Call</h3>
    <h4>Adams_ka@gmail.com</h4>
    <h6>started 3min ago</h6>
    </v-col>
    <v-col>
        <v-row>
          <v-avatar color="#ffffff00" size="62">
      <span class="white--text headline">62</span>
    </v-avatar>
      <v-avatar color="orange" size="62">
      <span class="white--text headline">62</span>
    </v-avatar>
        </v-row>
    </v-col>
    <v-col>
         <v-btn  outlined color="white" >
             Your are Invited
         </v-btn>
    </v-col>
      <v-col>
        <v-btn class="ma-2" tile color="white">
      <v-icon left>mdi-video</v-icon> Join Now
    </v-btn>
    </v-col>
   </v-row>
  </v-card>



    <v-card
    height="auto"
    class="mx-auto "
    
  >
   <v-row class="pa-9">
    <v-avatar
    size="100"
    color="grey"
    >
      <v-icon large >mdi-forum</v-icon> 
    </v-avatar>
    <v-col>
    <h3>Overall Messages</h3>
    <h4>23467 this month</h4>
    </v-col>
    <v-col>

      <div class="vl"></div>

      </v-col>
        <v-avatar
    size="100"
    color="grey"
    >
      <v-icon large >mdi-send</v-icon> 
    </v-avatar>
    <v-col>
    <h3>Sent Messages</h3>
    <h4>23467 this month</h4>
    </v-col>
       <v-avatar
    size="100"
    color="grey"
    >

     <div class="vl"></div>

      <v-icon large >mdi-call-received</v-icon> 
    </v-avatar>
    <v-col>
    <h3>Receivied Messages</h3>
    <h4>23467 this month</h4>
    </v-col>
    
     
   </v-row>
  </v-card>

   <v-data-table
    :headers="headers"
    :items="desserts"
    class="elevation-1"
     show-select
  >
    <template v-slot:item.calories="{ item }">
     <!-- <v-chip :color="getColor(item.calories)" dark>{{ item.calories }}</v-chip> -->
      <v-avatar
    size="40"
    >
      <img
        src="https://cdn.vuetifyjs.com/images/john.jpg"
        alt="John"
      >
    </v-avatar>
    </template>
  </v-data-table>
        
    </div>
</template>

<script>
export default {
    name:'listusers',
    data(){
      return{
         headers: [
          {
            text: 'Dessert (100g serving)',
            align: 'left',
            sortable: false,
            value: 'name',
          },
          { text: 'Calories', value: 'calories' },
          { text: 'Fat (g)', value: 'fat' },
          { text: 'Carbs (g)', value: 'carbs' },
          { text: 'Protein (g)', value: 'protein' },
          { text: 'Iron (%)', value: 'iron' },
        ],
        desserts: [
          {
            name: 'Frozen Yogurt',
            calories: 159,
            fat: 6.0,
            carbs: 24,
            protein: 4.0,
            iron: '1%',
          },
        ]
      }
    },
       methods: {
      getColor (calories) {
        if (calories > 400) return 'red'
        else if (calories > 200) return 'orange'
        else return 'green'
      },
       }
    
}
</script>

<style >
    .cardbg{
        background: #833ab4;  /* fallback for old browsers */

background: -webkit-linear-gradient(to right,#fd1d1d, #fcb045);
background: linear-gradient(to right, #fd1d1d, #fcb045); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

    }

    .vl {
  border-left: 1px solid grey;
  height: 50px;
}
</style>