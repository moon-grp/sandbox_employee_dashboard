<template>
  <v-app>
    <appbar />
    
      <v-row class="pa-5">
      <v-col sm="12" lg="3">
      <sidemenu  />
        </v-col>
        <v-col sm="12" lg="9">
      <listusers />
        </v-col>
           <v-btn
              absolute
              dark
              fab
              bottom
              right
              color="pink"
            >
              <v-icon>mdi-plus</v-icon>
            </v-btn>
      </v-row>
  
    
  </v-app>
</template>

<script>
import appbar from './components/appbar'
import sidemenu from './components/sidemenu'
import listusers from './components/listusers'

export default {
  name: 'App',
  components: {
    appbar,
    sidemenu,
    listusers
  },
  data: () => ({
    //
  }),
};
</script>
