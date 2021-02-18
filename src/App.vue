<template>
  <div id="app">
  <v-app>
    <v-content>
      <app-body></app-body>
    </v-content>
    <app-footer></app-footer>
  </v-app>
 </div>
</template>

<script>
import Body from './components/HomeComponent.vue';
import Footer from './components/footerComponent.vue';

export default {
  name: 'App',

  components: {
    appBody: Body,
    appFooter: Footer,
  },
};
</script>
