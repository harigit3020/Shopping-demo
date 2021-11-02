<template>
  <v-app>
    <v-layout row wrap>
      <v-container>
        <v-card>
          <v-card-title id="title">
            <v-icon small class="iconn" left>mdi-solid</v-icon> New
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
                    <v-card>
                      <v-img
                        :src="card.src"
                        class="white--text align-end"
                        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                        height="200px"
                      >
                      </v-img>
                      <div v-text="card.subtitle" class="names"></div>
                      <div v-text="card.price" class="price"></div>
                      <v-rating
                        :value="4.5"
                        color="amber"
                        dense
                        half-increments
                        readonly
                        size="14"
                      ></v-rating>
                    </v-card>
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

export default {
  name: "Home",
  components: {},
  data: () => {
    return {
      cards: [
        {
          subtitle: "Pre-fab homes",
          price: "$80.40",
          src: "https://cdn.vuetifyjs.com/images/cards/house.jpg",
          flex: 2,
        },
        {
          subtitle: "Favorite road trips",
          price: "$80.40",
          src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
          flex: 2,
        },
        {
          subtitle: "Best airlines",
          price: "$60.40",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 2,
        },
        {
          subtitle: "Best airlines",
          price: "$80.40",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 2,
        },
        {
          subtitle: "Best airlines",
          price: "$80.40",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 2,
        },
        {
          subtitle: "Best airlines",
          price: "$80.40",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 2,
        },
        {
          subtitle: "Best airlines",
          price: "$80.40",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 2,
        },
        {
          subtitle: "Best airlines",
          price: "$80.40",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 2,
        },
        {
          subtitle: "Best airlines",
          price: "$80.40",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 2,
        },
        {
          subtitle: "Best airlines",
          price: "$80.40",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 2,
        },
        {
          subtitle: "Best airlines",
          price: "$80.40",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 2,
        },
        {
          subtitle: "Best airlines",
          price: "$80.40",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 2,
        },
        {
          subtitle: "Best airlines",
          price: "$80.40",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 2,
        },
        {
          subtitle: "Best airlines",
          price: "$80.40",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 2,
        },
        {
          subtitle: "Best airlines",
          price: "$80.40",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 2,
        },
      ],
    };
  },
};
</script>
<style scoped>
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
  font-size: 20px;
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
