<template>
  <div id="app">
    <ApartmentsList :items="apartments" />
  </div>
</template>

<script>
import apartments from "./components/apartment/apartments";

import ApartmentsList from "./components/apartment/ApartmentsList.vue";

export default {
  name: "App",
  components: { ApartmentsList },

  data() {
    return {
      apartments,
      apartment: {
        id: "4461sdsdsdsdd",
        title: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. ",
        descr:
          "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Asperiores minima vitae amet in atque, at itaque, sed, officia praesentium quidem molestias. Consequatur molestiae, totam natus iusto ratione fuga est dicta.",
        price: 2155,
        rating: 3.5,
        location: { city: "London" },
        owner: {
          name: "Nik",
          phone: "050-45-82-753",
          email: "Nik-Best@ukr.net",
        },
      },
    };
  },
};
</script>

<style>
@font-face {
  font-family: Montserrat;
  src: url("./assets/fonts/Montserrat-Medium.ttf");
}

@font-face {
  font-family: Montserrat;
  src: url("./assets/fonts/Montserrat-Bold.ttf");
  font-weight: 700;
}

@font-face {
  font-family: Montserrat;
  src: url("./assets/fonts/Montserrat-ExtraBold.ttf");
  font-weight: 800;
}

#app {
  font-family: Montserrat, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
