<template>
  <v-container>
      <h2 class="display-2 black--text text-center font-weight-bold mb-3">CONTACT ME</h2>
    <v-row class="text-center">
     <v-col>
       <v-card elevation="24"
       color="#424242"
       class="mx-auto dark"
        style="max-width: 25rem;">
        <div></div>
         <v-avatar
                  class="elevation-12 mb-3 mt-2 adjustPhoto"
                  size="50"
                  >
                  <v-img src="@/assets/myphoto.png"></v-img>
                  </v-avatar>
        <form class="pa-4">
        <v-text-field
        height="1px"
        v-model="name"
        :error-messages="nameErrors"
        :counter="10"
        label="Name"
        rounded
        filled
        color="amber darken-3"
        background-color="white"
        required
        @input="$v.name.$touch()"
        @blur="$v.name.$touch()"
        ></v-text-field>
        <v-text-field
        v-model="email"
        :error-messages="emailErrors"
        label="E-mail"
        rounded
        filled
        background-color="white"
        color="amber darken-3"
        required
        @input="$v.email.$touch()"
        @blur="$v.email.$touch()"
        ></v-text-field>
        <v-textarea
        v-model="message"
        :error-messages="messageErrors"
        label="Message"
        :counter="200"
        color="amber darken-3"
        background-color="white"
        filled
        required
        @input="$v.message.$touch()"
        @blur="$v.message.$touch()"
        ></v-textarea>

    <v-btn rounded
    :disabled="$v.$anyErorr || !email || !message"
    class="mr-5"
    @click="submit"
    color="#FFE0B2">
    submit
    </v-btn>
    <v-btn rounded  @click="clear" color="#FFE0B2">clear</v-btn>
  </form>
  </v-card>
     </v-col>
    </v-row>
  </v-container>
</template>

<script>
// eslint-disable-next-line import/no-unresolved
import { validationMixin } from 'vuelidate';
import { required, maxLength, email } from 'vuelidate/lib/validators';

export default {
  mixins: [validationMixin],

  validations: {
    name: { required, maxLength: maxLength(10) },
    email: { required, email },
    message: { required, maxLength: maxLength(200) },
  },

  data: () => ({
    name: '',
    email: '',
    message: '',
  }),

  computed: {
    messageErrors() {
      const errors = [];
      if (!this.$v.message.$dirty) return errors;
      if (!this.$v.message.required) errors.push('Message feild is required');
      if (!this.$v.message.maxLength) errors.push('Message must not exceed 200 words');
      return errors;
    },
    nameErrors() {
      const errors = [];
      if (!this.$v.name.$dirty) return errors;
      if (!this.$v.name.maxLength) errors.push('Name must be at most 10 characters long');
      if (!this.$v.name.required) errors.push('Name is required.');
      return errors;
    },
    emailErrors() {
      const errors = [];
      if (!this.$v.email.$dirty) return errors;
      if (!this.$v.email.email) errors.push('Must be valid e-mail');
      if (!this.$v.email.required) errors.push('E-mail is required');
      return errors;
    },
  },

  methods: {
    submit() {
      this.$v.$touch();
    },
    clear() {
      this.$v.$reset();
      this.name = '';
      this.email = '';
      this.message = '';
    },
  },
};
</script>
<style scoped>
h3 {
  color: black;
}
.textColor {
  color: "#385F73"
}
</style>
