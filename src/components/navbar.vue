<template>
  <nav>
    <!--Navbar-->
    <v-app-bar class="white" dense>
      <v-app-bar-title>
        <span id="title" class="font-wieght-bold"
          >Trend<span class="t2">Shop</span></span
        >
      </v-app-bar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-xs-only">
        <span class="my-3 mx-10"
          ><router-link to="#" id="link"
            ><p class="grey--text">Home</p></router-link
          ></span
        >
        <span class="my-3  mx-10"
          ><router-link to="#" id="link"
            ><p class="grey--text">Products</p></router-link
          ></span
        >
        <span class="my-3 mx-10"
          ><router-link to="#" id="link"
            ><p class="grey--text">Shop</p></router-link
          ></span
        >
        <span class="my-3  mx-10"
          ><router-link to="#" id="link"
            ><p class="grey--text">Pages</p></router-link
          ></span
        >
      </v-toolbar-items>
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>
    <!--Navbar ends-->
  </nav>
</template>
<script>
export default {
  data: () => {
    return {};
  },
};
</script>

<style>
span{
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
#title {
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  font-weight: bold;
  text-transform: capitalize;
}
.t2 {
  color: red;
}
#link {
  text-decoration: none;
}
</style>
