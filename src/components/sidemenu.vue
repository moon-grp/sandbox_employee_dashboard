<template>
    <div>
        <v-card
    class="mx-auto"
    max-width="300"
    tile
  >
    <v-list shaped>
     
           <v-avatar tile class="">
      <img
        src="https://cdn.vuetifyjs.com/images/john.jpg"
        alt="John"
      >
    </v-avatar>
    <h4 class=""> Welcome olumide </h4>
    <h5>Super Admin</h5>
       <v-divider></v-divider>
      <v-list-item-group v-model="item" color="primary">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
        >
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item-content>
          
        </v-list-item>
      </v-list-item-group>
    </v-list>
    
    <v-card-actions >
        <v-row align="center" justify="center">
      <v-btn text>Full Report</v-btn>
        </v-row>
    </v-card-actions>
  </v-card>
    </div>
</template>

<script>
export default {
    name: "sidemenu",
    data(){
        return{
            item: 1,
      items: [
        { text: 'Overview', icon: 'mdi-widgets' },
        { text: 'Reservation', icon: 'mdi-bookmark' },
        { text: 'Meeting', icon: 'mdi-credit-card-outline' },
        { text: 'Customers', icon: 'mdi-account-multiple' },
        { text: 'Ticket', icon: 'mdi-assistant' },
        { text: 'Message', icon: 'mdi-forum' },
        { text: 'Profile', icon: 'mdi-account' },
      ],
        }
    }

    
}
</script>

<style >
    
</style>