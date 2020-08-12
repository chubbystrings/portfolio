<template>
    <div>
        <v-btn
          color="orange"
          absolute
          dark
          bottom
          right
          fab
          class=""
          @click="$vuetify.goTo('#hero')"
        >
          <v-icon>mdi-chevron-up</v-icon>
        </v-btn>
        <section id="hero">
        <v-row no-gutters>
          <v-img
            :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
            src="@/assets/artoftravel.jpg"
          >
            <v-theme-provider dark>
              <v-container fill-height>
                  <v-avatar
                  class="elevation-12 adjustPhoto"
                  size="50"
                  >
                  <v-img src="@/assets/myphoto.png"></v-img>
                  </v-avatar>
                  <v-btn
                  class="adjustBlogBtn"
                  dark
                  fab
                  color="orange"
                   href="https://my-blog-cms-33634.web.app"
                >
                  BLOG
                </v-btn>
                <v-row
                  align="center"
                  class="white--text mx-auto"
                  justify="center"
                >
                  <v-col
                    class="white--text text-center"
                    cols="12"
                    tag="h1"
                  >
                    <span
                      class="font-weight-light"
                      :class="[$vuetify.breakpoint.smAndDown ? 'display-1' : 'display-2']"
                      style="color: #FFE0B2;"
                    >
                      WELCOME TO
                    </span>

                    <br>

                    <span
                      :class="[$vuetify.breakpoint.smAndDown ? 'display-3': 'display-4']"
                      class="font-weight-black"
                      style="color: #FFE0B2;"
                    >
                      MY PAGE
                    </span>

                  </v-col>

                  <v-btn
                    class="align-self-end"
                    fab
                    outlined
                    @click="$vuetify.goTo('#about-me')"
                  >
                    <v-icon color="#FFE0B2">mdi-chevron-double-down</v-icon>
                  </v-btn>
                </v-row>
              </v-container>
            </v-theme-provider>
          </v-img>
        </v-row>
      </section>

      <section id="about-me" style="">
        <div class="py-12"></div>

        <v-container class="text-center">
          <h2 class="display-2 font-weight-bold mb-3">ABOUT ME</h2>

          <v-responsive
            class="mx-auto mb-8"
            width="56"
          >
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>
           <v-avatar
            class="elevation-12 mb-12"
            size="128"
          >
            <v-img src="@/assets/myphoto.png"></v-img>
          </v-avatar>

          <div></div>

          <v-responsive
            class="mx-auto title font-weight-light mb-8"
            max-width="720"
          >
            Okwor Emeka Martins AKA chubbyCode as he is
            fondly called by close associates holds a degree in food Science & Technology
            from the federal University of Technology Owerri Imo State, Nigeria
            He found his love for programming after watching series of
            youtube videos on how to create web pages in 2019.
            Emeka is a self taught javascript fullstack developer
            who also has some knowlege with backend technologies like PHP and
            LARAVEL.
            Emeka loves to play the guitar during his leisures and
            is a lover of jazz and Afro pop music.
          </v-responsive>

          <v-btn
            class="align-self-end"
            fab
            outlined
            @click="$vuetify.goTo('#features')"
            >
            <v-icon>mdi-chevron-double-down</v-icon>
            </v-btn>
        </v-container>

        <div class="py-12"></div>
      </section>

      <section
        id="features"
        class="grey lighten-3"
      >
        <div class="py-12"></div>

        <v-container class="text-center">
          <h2 class="display-2 font-weight-bold mb-3">PERSONAL PROJECTS</h2>

          <v-responsive
            class="mx-auto mb-12"
            width="56"
          >
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>

          <v-row>
            <v-col
              cols="12"
              md="4"
            >
            </v-col>
        <v-carousel hide-delimiters show-arrows light>
            <v-carousel-item
            v-for="(item,i) in features"
            :key="i"
            reverse-transition="fade-transition"
            transition="fade-transition"
            >
            <v-card
            class="py-12 px-4 mx-auto"
            color=""
            elevation="15"
            width="344"
            height="500"
            >
            <v-theme-provider dark>
                <div>
                <v-avatar
                    :color="`#${Math.floor(Math.random() * 16777215).toString(16)}`"
                    size="88"
                >
                </v-avatar>
                </div>
            </v-theme-provider>

            <v-card-title
                class="justify-center font-weight-black text-uppercase"
                v-text="item.title"
            ></v-card-title>
              <small>{{item.tech}}</small>
            <v-card-text
                class="subtitle-1"
                v-text="item.text"
            >
            </v-card-text>
            <v-card-actions>
                <v-btn
                class="btnClass"
                :href="item.url" target="_blank"
                text>
                Go To Page
                </v-btn>
            </v-card-actions>
            </v-card>
        </v-carousel-item>
  </v-carousel>
            <v-col cols="12">
            </v-col>
        </v-row>
    </v-container>

        <div class="py-12"></div>
      </section>

      <section id="stats">
        <v-parallax
          src="https://images.unsplash.com/photo-1487017159836-4e23ece2e4cf?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1951&q=80"
        >
          <v-container fill-height class="text-center">
            <v-row class="mx-auto">
                <v-col cols="12" class="text-center">
                    <h2
                    class="display-2 font-weight-bold mb-3"
                    style="color: #FFE0B2;"
                    >
                    STACK AND TOOLS
                    </h2>
                </v-col>
              <v-col
                v-for="[value] of stats"
                :key="value"
                cols="12"
                md="3"
              >
                <div class="text-center">
                  <div
                    class="display-1 font-weight-black mb-2"
                    v-text="value"
                    style="color: #FFE0B2;"
                  ></div>
                </div>
              </v-col>
            </v-row>
          </v-container>
        </v-parallax>
      </section>

      <!-- <section id="blog">
        <div class="py-12"></div>

        <v-container>
          <h2 class="display-2 font-weight-bold mb-3 text-uppercase text-center">Blog</h2>

          <v-responsive
            class="mx-auto mb-12"
            width="56"
          >
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>

          <v-row>
            <v-col
              v-for="({ src, text, title }, i) in articles"
              :key="i"
              cols="12"
              md="4"
            >
              <v-img
                :src="src"
                class="mb-4"
                height="275"
                max-width="100%"
              ></v-img>

              <h3
                class="font-weight-black mb-4 text-uppercase"
                v-text="title"
              ></h3>

              <div
                class="title font-weight-light mb-5"
                v-text="text"
              ></div>

              <v-btn
                class="ml-n4 font-weight-black"
                text
              >
                Continue Reading
              </v-btn>
            </v-col>
          </v-row>
        </v-container>

        <div class="py-12"></div>
      </section> -->
    <section id="contact" class="grey lighten-3">
        <div class="py-12"></div>
     <app-contact></app-contact>
    </section>
    </div>
</template>
<script>

import ContactForm from './contactMeComponent.vue';

export default {
  name: 'App',

  data() {
    return {
      articles: [
        {
          src: 'https://images.unsplash.com/photo-1423784346385-c1d4dac9893a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80',
          title: 'Mobile first & Responsive',
          text: 'Phasellus lorem enim, luctus ut velit eget, convallis egestas eros. Sed ornare ligula eget tortor tempor, quis porta tellus dictum.',
        },
        {
          src: 'https://images.unsplash.com/photo-1475938476802-32a7e851dad1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80',
          title: 'Think outside the box',
          text: 'Nam ut leo ipsum. Maecenas pretium aliquam feugiat. Aenean vel tempor est, vitae tincidunt risus. Sed sodales vestibulum nibh.',
        },
        {
          src: 'https://images.unsplash.com/photo-1416339442236-8ceb164046f8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1892&q=80',
          title: 'Small changes, big difference',
          text: 'Vestibulum in dictum velit, in rhoncus nibh. Maecenas neque libero, interdum a dignissim in, aliquet vitae lectus. Phasellus lorem enim, luctus ut velit eget.',
        },
      ],
      features: [
        {
          icon: 'mdi-account-group-outline',
          title: 'WEBCOLORS',
          text: 'Webcolors is a search engine  web app for html colors with over 146 colors available in hex, rgba format ',
          tech: 'VUE JS',
          url: 'https://master--webcolors.netlify.com/',
        },
        {
          icon: 'mdi-update',
          title: 'NOTES APP',
          text: 'Notes app is a simple crud application for storing short notes and was built with vue js and firsbase',
          tech: 'VUE JS',
          url: 'https://notes-app-38c1f.firebaseapp.com',
        },
        {
          icon: 'mdi-shield-outline',
          title: 'WEBCOLORS API',
          text: 'Webcolors API is an application to access over 146 html colors including their hex and rgb values. It was built with Noe Js',
          tech: 'NODE JS',
          url: 'https://github.com/chubbystrings/web-colors_api',
        },
        {
          icon: 'mdi-shield-outline',
          title: 'CALCULATOR',
          text: 'Calculator app is a simple calculator that can also check if a number is Narcissistic, built with Vue Js',
          tech: 'VUE JS',
          url: 'https://calculator-app-6a0dd.firebaseapp.com',
        },
        {
          icon: 'mdi-shield-outline',
          title: 'UTME QUIZ GAME',
          text: 'UTME QUIZ GAME APP is application for students preparing for UTME exams with questions from subjects like Maths, English etc. This app was built vanila javascript and ALOC past questions API',
          tech: 'JAVASCRIPT',
          url: 'https://quiz-app-for-utme.netlify.com',
        },

        {
          icon: 'mdi-shield-outline',
          title: 'PORTFOLIO PAGE',
          text: 'A simple portfolio page built with Jquery',
          tech: 'JQUERY',
          url: 'https://jquery-portfolio-page.netlify.com',
        },

        {
          icon: 'mdi-shield-outline',
          title: 'MOCKSHOP API',
          text: 'Mockshop API is a simple online store API It was built with NODE JS and Swagger for API testing',
          tech: 'NODE JS & SWAGGER',
          url: 'https://mockshop-product.herokuapp.com/api-docs',
        },

        {
          icon: 'mdi-shield-outline',
          title: 'TEAMPLAY',
          text: 'Teamplay is a social web app built for the workplace, Users can create article posts, gif posts, comment, like posts etc',
          tech: 'NODE JS AND VUE JS',
          url: 'https://teamplay-app-e48a7.firebaseapp.com/',
        },
        {
          icon: 'mdi-shield-outline',
          title: 'FITAZ',
          text: 'Fitaz app is a social web app for fitness enthusiasts, where users in same location can connect with each other for fitness activities',
          tech: 'PHP OOP',
          url: 'http://emekaokwor.com/fitaz',
        },

        {
          icon: 'mdi-shield-outline',
          title: 'PUNTER MASTERS',
          text: 'Punter masters is a web app that connects bettors together, share betcode and talk about betting',
          tech: 'NODE JS, VUE JS AND FIREBASE',
          url: 'https://punter-matsers.web.app',
        },

      ],
      stats: [
        ['HTML 5'],
        ['CSS'],
        ['JAVASCRIPT'],
        ['PHP'],
        ['NODE JS'],
        ['VUE JS'],
        ['LARAVEL'],
        ['GIT'],
        ['TRAVIS CI'],
        ['SWAGGER'],
        ['POSTGRES'],
        ['MONGO DB'],
        ['MYSQL'],
        ['REST API'],
        ['JQUERY'],
      ],
      pagination: {
        page: 1,
        rowsPerPage: 3,
        visible: 5,
      },
    };
  },


  components: {
    appContact: ContactForm,
  },
};
</script>
<style scoped>
.adjustPhoto {
  position: absolute;
  top: 0.3rem;
  left: 0.2rem;
}

.adjustBlogBtn {
  position: absolute;
  top: 0.3rem;
  right: 0.2rem;
}

.btnClass {
  position: absolute;
  bottom: 0.2rem;
  left: 0;
  right: 0;
  margin: 0, auto;
}
.fixedBtn {
  position: fixed;
  bottom: 0.2rem;
  right: 0.4rem;
  z-index: 1000;
}
</style>
