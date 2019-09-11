<template>
    <div class="font">

         <v-row>
    <v-col>
      <h1>Messages</h1>
    </v-col>
    <v-col align="end">
       <v-btn class="mr-6" color="primary">All</v-btn>
      <v-btn class="mr-1">Unread</v-btn>
       <v-btn>Important</v-btn>
    </v-col>
  </v-row>
         <v-card
    class=" cardbg "
    height="auto"
  >
 
   <v-row class="pa-8">
    <v-avatar
    size="80"
    >
      <img
        src="https://cdn.vuetifyjs.com/images/john.jpg"
        alt="John"
      >
    </v-avatar>
    <v-col cols="">
    <h2 class="white--text" >Sales Presentation - Live Group Call</h2>
    <h3 class="white--text">Adams_ka@gmail.com</h3>
    <p class="white--text" >started 3min ago</p>
    </v-col>
    <v-col cols="">
        <v-row>
              <v-btn
              outlined
              color="white"
              fab
            > <h1>A</h1>
            </v-btn>
           <v-btn
            class="ml-n1 zd"
              outlined
              color="white"
              fab
            > <h1>k</h1>
            </v-btn>
             <v-btn
              outlined
              color="white"
              fab
            > <h1>d</h1>
            </v-btn>
             <v-btn
              outlined
              color="white"
              fab
            > <h1>v</h1>
            </v-btn>
        </v-row>
    </v-col>
    <v-col class="pt-5">
         <v-btn  outlined color="white" >
             Your are Invited
         </v-btn>
    </v-col>
      <v-col>
        <v-btn class="ma-2" tile color="white">
      <v-icon left color="grey">mdi-video</v-icon> Join Now
    </v-btn>
    </v-col>
   </v-row>
  </v-card>



    <v-card
    height="auto"
    class="mx-auto  my-3"
    
  >
   <v-row class="pa-9">
    <v-avatar
    size="90"
    color="#BBDEFB"
    >
      <v-icon large color="blue darken-4" >mdi-forum</v-icon> 
    </v-avatar>
    <v-col class="pt-6">
    <h3>Overall Messages</h3>
    <h4>23467 this month</h4>
    </v-col>
    <v-col>

      <div class="vl"></div>

      </v-col>
        <v-avatar
    size="90"
    color="#BBDEFB"
    >
      <v-icon large color="blue darken-4" >mdi-send</v-icon> 
    </v-avatar>
    <v-col class="pt-6">
    <h3>Sent Messages</h3>
    <h4>23467 this month</h4>
    </v-col>
    <v-col>
    <div class="vl"></div>
    </v-col>
       <v-avatar
    size="90"
    color="#BBDEFB"
    >
      <v-icon large color="blue darken-4" >mdi-call-received</v-icon> 
    </v-avatar>
    <v-col class="pt-6">
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
.font{
  font-size: 9px
}
</style>