<template>
      <v-footer
      class="justify-center"
      color="#292929"
    >
    <v-card
      color="transparent"
      flat
      tile
    >
      <v-card-title class="py-2 centerElements " >
        <strong class="subheading">Connect with me on my social networks</strong>
        <div>
        <v-btn
        text
        href="https://facebook.com/chubbystrings"
        target="_blank"
        color="#FFE0B2">
          <v-icon size="24px">mdi-facebook</v-icon>
        </v-btn>
        <v-btn
        text
        target="_blank"
        href="https://twitter.com/chubby_code"
        color="#FFE0B2"
        >
          <v-icon size="24px">mdi-twitter</v-icon>
        </v-btn>
        <v-btn
        text
        target="_blank"
        color="#FFE0B2"
        href="https://linkedin.com/in/emekaokwor"
        >
          <v-icon size="24px">mdi-linkedin</v-icon>
        </v-btn>
        <v-btn
        href="https://github.com/chubbystrings"
        text
        target="_blank"
        color="#FFE0B2">
          <v-icon size="24px">mdi-git</v-icon>
        </v-btn>
        <v-btn
        href="https://my-blog-cms-33634.web.app"
        text
        target="_blank"
        color="#FFE0B2">
          BLOG
        </v-btn>
        </div>
        <v-spacer></v-spacer>
      </v-card-title>
       <div class="title font-weight-light grey--text text--lighten-1 text-center">
        &copy; {{ (new Date()).getFullYear() }} — Configured by ChubbyCode
      </div>
    </v-card>
    </v-footer>
</template>
<script>
export default {
  props: ['background'],
  data() {
    return {
      icons: [
        'fab mdi- fa-facebook',
        'fab fa-twitter',
        'fab fa-google-plus',
        'fab fa-linkedin',
        'fab fa-instagram',
      ],
      bcolor: 'black',
    };
  },

};
</script>
<style scoped>
.centerElements {
   display: flex;
   justify-content: center;
}
.centerElements > * {
  color: #FFE0B2
}
</style>
