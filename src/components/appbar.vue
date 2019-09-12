<template>
    <div>
       <v-toolbar>
    


       <v-container
      mx-auto
      py-0
    >
     <v-layout>
         <v-toolbar-items>
      <v-btn  class="mr-12" text>
          Boardash
          </v-btn>
         </v-toolbar-items>
 
        <v-text-field
          append-icon="mdi-magnify"
          flat
          placeholder="Search people, messages and ticket"
          hide-details
          solo-inverted
          style="max-width: 600px;"
        />
<v-spacer />
      <v-toolbar-items>
       
        <v-btn depressed class="mr-12" color="white" >
            <v-icon left dark>mdi-bell</v-icon>
          Set Alert
          </v-btn>
        
    <v-avatar class="mr-5">
      <img
        src="https://cdn.vuetifyjs.com/images/john.jpg"
        alt="John"
      >
    </v-avatar>
    <h4 class="mt-3">olumide adebayo</h4>
      <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on }">
          <v-btn icon v-on="on">
            <v-icon>mdi-plus-circle-outline</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item
            v-for="n in 5"
            :key="n"
            @click="() => {}"
          >
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
      </v-toolbar-items>
     </v-layout>
       </v-container>
    </v-toolbar>
    </div>
</template>


<script>
import mdiDelete from '@mdi/js'
export default {
     name: 'appbar',
     data(){
         return{
             icons:{
                 mdiDelete
             }
         }
     }
}
</script>


<style  scoped>

</style>