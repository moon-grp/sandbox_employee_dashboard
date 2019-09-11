<template>
  <v-app>
    <appbar />
    <v-container>
      <sidemenu />
      <listusers />
    </v-container>
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
