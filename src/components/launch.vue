<template>
  <v-app>
    <Navbar />
    <v-carousel :show-arrows="false">
      <v-carousel-item
        v-for="(item, i) in items"
        :key="i"
        :src="item.src"
      ></v-carousel-item>
    </v-carousel>
    <h1 class="title1">NEW SEASON</h1>
    <h1 class="title2">NEW BRAND COLLECTIONS</h1>
    <p class="subs">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum voluptate
      libero magnam quidem quam. Pariatur voluptates ab sunt iure similique
      recusandae, eveniet quod placeat consequuntur exercitationem libero
      perspiciatis incidunt molestias.
    </p>
    <v-btn class="button" small color="pink"> SHOP NOW</v-btn>
  </v-app>
</template>
<script>
import Navbar from "../components/navbar.vue";
export default {
  name: "Launch",
  components: {
    Navbar,
  },
  data: () => {
    return {
      items: [
        {
          src: require("../assets/images/shop.jpg"),
        },
        {
          src: require("../assets/images/shop.jpg"),
        },
        {
          src: require("../assets/images/shop.jpg"),
        },
        {
          src: require("../assets/images/shop.jpg"),
        },
      ],
    };
  },
};
</script>
<style scoped>
* {
  margin: 0;
  padding: 0;
}
.body {
  background-image: linear-gradient(to top, black 0%, gray 100%);
  font-family: "Roboto", sans-serif;
}
.title1 {
  position: absolute;
  left: 8%;
  top: 25%;
  color: white;
}
.title2 {
  position: absolute;
  left: 8%;
  top: 32%;
  color: white;
}
.subs {
  position: absolute;
  left: 8%;
  top: 40%;
  right: 60%;
  color: white;
}
.button {
  position: absolute;
  color: white;
  top: 60%;
  left: 8%;
}
</style>
