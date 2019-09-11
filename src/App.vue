<template>
  <v-app>
    <appbar />
    <v-container>
      <sidemenu />
    </v-container>
  </v-app>
</template>

<script>
import appbar from './components/appbar'
import sidemenu from './components/sidemenu'

export default {
  name: 'App',
  components: {
    appbar,
    sidemenu
  },
  data: () => ({
    //
  }),
};
</script>
