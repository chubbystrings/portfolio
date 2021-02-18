<template>
  <v-container>
      <h2 class="display-2 black--text text-center font-weight-bold mb-3">CONTACT ME</h2>
    <v-row class="text-center">
     <v-col>
        <!-- <iframe class="responsive-iframe" src="https://docs.google.com/forms/d/e/1FAIpQLScro9ERPlnhJlKvVieJjIOjSA_zIR0V4jKVWvR01A25yzadbw/viewform?embedded=true"  frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe> -->
        <div class="my-2">
            <v-btn
              color="orange"
              fab
              x-large
              dark
              class="ma-2"
              outlined
              href="https://forms.gle/rWr7zrUPyi4p5ShX7"
            >
              <v-icon>mdi-email-send-outline</v-icon>
            </v-btn>
          </div>
     </v-col>
    </v-row>
  </v-container>
</template>

<script>
// eslint-disable-next-line import/no-unresolved
export default {

};
</script>
<style scoped>
.responsive-iframe {
    height: 90vh;
    width: 70vw;
    padding: 1rem;
    margin: 2rem auto;
}
</style>
