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
           <v-list-item-content
            absolute
                  bottom
                  left
           >
               <v-list-item-title>
                   lol
               </v-list-item-title>
           </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
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
        { text: 'OVerview', icon: 'mdi-clock' },
        { text: 'Reservation', icon: 'mdi-account' },
        { text: 'Meeting', icon: 'mdi-flag' },
        { text: 'Customers', icon: 'mdi-flag' },
        { text: 'Ticket', icon: 'mdi-flag' },
        { text: 'Message', icon: 'mdi-flag' },
        { text: 'Profile', icon: 'mdi-flag' },
      ],
        }
    }

    
}
</script>

<style >
    
</style>