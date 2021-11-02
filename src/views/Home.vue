<template>
  <v-app>
    <Launch class="body" />
    <Discover />
    <v-layout row wrap>
      <v-container>
        <v-card>
          <v-card-title id="title">
            <v-icon small color="red" left>mdi-solid</v-icon> New
            Arrivals</v-card-title
          >
          <v-tabs color="red accent-3" left>
            <v-tab class="subs">All</v-tab>
            <v-tab class="subs">Cloths</v-tab>
            <v-tab class="subs">Shoes</v-tab>
            <v-tab class="subs">Bags</v-tab>
            <v-tab class="subs">Jewellary</v-tab>
            <v-tab class="subs">Accesories</v-tab>
            <v-tab-item v-for="n in 6" :key="n">
              <v-container fluid>
                <v-row>
                  <v-col
                    v-for="card in cards"
                    :key="card.title"
                    :cols="card.flex"
                  >
                    <v-hover>
                      <template v-slot:default="{ hover }">
                        <v-card :elevation="hover ? 24 : 6">
                          <v-img
                            :src="card.src"
                            class="white--text align-end"
                            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                            height="200px"
                          >
                          </v-img>
                          <div v-text="card.subtitle" class="names mx-2"></div>
                          <div v-text="card.price" class="price mx-2"></div>
                          <v-rating
                            :value="4.5"
                            color="amber"
                            dense
                            half-increments
                            readonly
                            size="14"
                          ></v-rating>
                        </v-card>
                      </template>
                    </v-hover>
                  </v-col>
                </v-row>
              </v-container>
            </v-tab-item>
          </v-tabs>
        </v-card>
      </v-container>
    </v-layout>
  </v-app>
</template>
<script>
// @ is an alias to /src
import Launch from "../components/launch.vue";
import Discover from "../components/discover.vue";
export default {
  name: "Home",
  components: {
    Launch,
    Discover,
  },
  data: () => {
    return {
      cards: [
        {
          subtitle: "T-shirt Gray",
          price: "$80.40",
          src: require("../assets/images/grey-t-shirt.jpg"),
          flex: 2,
        },
        {
          subtitle: "Black Sneaker",
          price: "$20.40",
          src: require("../assets/images/black-sneakers-with-white-sole.jpg"),
          flex: 2,
        },
        {
          subtitle: "Headphone Black",
          price: "$60.40",
          src: require("../assets/images/wireless-headphones.jpg"),
          flex: 2,
        },
        {
          subtitle: " Backpack Black",
          price: "$40.40",
          src: require("../assets/images/backpack-in-black.jpg"),
          flex: 2,
        },
        {
          subtitle: "T-shirt Gray",
          price: "$80.40",
          src: require("../assets/images/grey-t-shirt.jpg"),
          flex: 2,
        },
        {
          subtitle: "Black Sneaker",
          price: "$20.40",
          src: require("../assets/images/black-sneakers-with-white-sole.jpg"),
          flex: 2,
        },
        {
          subtitle: "Headphone Black",
          price: "$60.40",
          src: require("../assets/images/wireless-headphones.jpg"),
          flex: 2,
        },
        {
          subtitle: " Backpack Black",
          price: "$40.40",
          src: require("../assets/images/backpack-in-black.jpg"),
          flex: 2,
        },
        {
          subtitle: "Black Sneaker",
          price: "$20.40",
          src: require("../assets/images/black-sneakers-with-white-sole.jpg"),
          flex: 2,
        },
        {
          subtitle: "Headphone Black",
          price: "$60.40",
          src: require("../assets/images/wireless-headphones.jpg"),
          flex: 2,
        },
        {
          subtitle: "T-shirt Gray",
          price: "$80.40",
          src: require("../assets/images/grey-t-shirt.jpg"),
          flex: 2,
        },
        {
          subtitle: "Black Sneaker",
          price: "$20.40",
          src: require("../assets/images/black-sneakers-with-white-sole.jpg"),
          flex: 2,
        },
        {
          subtitle: "Headphone Black",
          price: "$60.40",
          src: require("../assets/images/wireless-headphones.jpg"),
          flex: 2,
        },
        {
          subtitle: " Backpack Black",
          price: "$40.40",
          src: require("../assets/images/backpack-in-black.jpg"),
          flex: 2,
        },
      ],
    };
  },
  methods: {
    hello(title) {
      alert(title);
    },
  },
};
</script>
<style scoped>
.body {
  background-image: linear-gradient(to top, black 0%, gray 100%);
  font-family: "Roboto", sans-serif;
}
#title {
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
}
.names {
  text-align: start;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  color: gray;
}
.price {
  text-align: start;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  font-size: 15px;
  color: gray;
}
.iconn {
  background-color: #ff1744;
}
.subs {
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  font-size: small;
  text-transform: capitalize;
  font-weight: bold;
}
</style>
