<template>
  <v-app>
    <v-app-bar
      class="elevation-0 mt-5 py-3 container"
      style="background-color: #302C42"
      elevation="4"
      absolute
      app
    >
      <v-row justify="space-between">
        <v-col cols="3" sm="3" md="3" lg="3" class="d-flex align-center">
          <div>
            <nuxt-link to="/" class="d-flex justify-center align-center">
              <v-img src="/logo.svg" max-width="80"></v-img>
              <v-img src="/Frame.svg" max-width="50" class="ml-2"></v-img>
            </nuxt-link>
          </div>
        </v-col>
        <v-col cols="12" sm="4" md="6" lg="6" align-self="center" class="menu-link">
          <div>
            <v-list style="background-color: inherit;" class="d-flex justify-center">
              <v-list-item v-for="item in items" class="text-center" :key="item.id" style="color: #ffffff">
                <v-list-item-content>
                  <nuxt-link class="menu--link__active" :to="'/'+ item.to"><span class="text-uppercase">{{ item.text }}</span></nuxt-link>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </div>
        </v-col>
        <v-col cols="12" sm="4" md="3" lg="3" align-self="center" class="menu-link">
          <div class="d-flex justify-center align-center">
            <v-btn small class="rounded-xxl mr-2">
              CONTACT US
            </v-btn>
            <BTNComponents text="JOIN HYDRA"/>
          </div>
        </v-col>
        <v-col cols="2" sm="2" md="2" lg="2" class="burger--menu" align-self="center">
          <div class="burger--menu-dev d-flex justify-center align-center">
            <v-img src="/burger-btn.svg"/>
          </div>
        </v-col>
      </v-row>
    </v-app-bar>

    <v-main style="background-color: #302C42">
      <v-container class="mt-10">
        <Nuxt/>
      </v-container>
    </v-main>
    <v-footer style="background-color: #302C42">
      <v-container>
        <FooterComponents/>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
import FooterComponents from "~/components/Footer.vue";
import BTNComponents from "~/components/BTN.vue";

export default {
  name: "SidebarComponents",
  components: {BTNComponents, FooterComponents},
  data() {
    return {
      items: [
        {
          id: 1,
          text: 'About',
          to: 'about'
        },
        {
          id: 2,
          text: 'Services',
          to: 'services'
        },
        {
          id: 3,
          text: 'Technologies',
          to: 'technologies'
        },
        {
          id: 4,
          text: 'How to',
          to: 'how-to'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;200;300;400;500;600;700;800;900&display=swap');

html, body, p, h1, h2, h3, h4, h5 {
  font-family: Monospaced;
}
a {
  text-decoration: none;
  color: #fff;
  font-family: Monospaced;
}
.burger--menu-dev{
  width: 30px;
  height: 30px;
}
.burger--menu{
  display: none;
}
.menu--link__active{
  font-size: 14px !important;
}
@media (max-width: 960px) {
  .menu-link{
    display: none;
  }
  .burger--menu{
    display: block;
  }
}
</style>
