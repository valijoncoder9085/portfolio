<template>
  <div>
    <v-row class="footer--section" align="center">
      <v-col cols="12" sm="2" md="2" lg="2" class="d-flex justify-center">
        <div class="d-flex align-center">
          <v-icon class="footer--logo" size="32">
            mdi-account
          </v-icon>
          <p class="footer--text text-uppercase ml-2 mb-0">Valijon <br><span class="footer--text__span"> Mizrofov</span></p>
        </div>
      </v-col>
      <v-col cols="12" sm="10" md="6" lg="6">
        <div class="d-flex justify-center">
          <ul class="footer--list">
            <li class="footer--list__item">about</li>
            <li class="footer--list__item">Pricing</li>
            <li class="footer--list__item">Company</li>
            <li class="footer--list__item">Blog</li>
          </ul>
        </div>
      </v-col>
      <v-spacer/>
      <v-col cols="12" sm="12" md="4" lg="4">
        <div class="d-flex justify-center">
          <ul class="footer--list">
            <li class="footer--list__item"><nuxt-link to="#"><v-icon class="footer--logo logo-facebook">mdi-facebook</v-icon></nuxt-link></li>
            <li class="footer--list__item"><nuxt-link to="#"><v-icon class="footer--logo logo-linkedin">mdi-linkedin</v-icon></nuxt-link></li>
            <li class="footer--list__item"><nuxt-link to="#"><v-icon class="footer--logo logo-google">mdi-google</v-icon></nuxt-link></li>
            <li class="footer--list__item">Copyright © 2023</li>
          </ul>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "FooterComponents",
  data(){
    return{

    }
  }
}
</script>

<style lang="scss" scoped>
.footer--section{
  color: #ffffff!important;
}
.footer--list{
  text-transform: capitalize;
  display: flex;
  .footer--list__item{
    margin: 0 10px;
    display: inline;
    font-size: 0.85rem;
    .logo-facebook:hover{
      color: #5e5ede;
      background-color: #fff;
      border-radius: 50%;
    }
    .logo-google:hover{
      color: yellow;
    }
    .logo-linkedin:hover{
      color: blue;
      background-color: #fff;
      border-radius: 50%;
      padding: 0;
    }
  }
}
.footer--logo{
  color: #fff;
}
.footer--text{
  color: #DD2242;
  .footer--text__span{
    color: #fff;
  }
}

</style>
