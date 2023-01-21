<template>
  <div id="app">
    <p>{{ text }}</p>
    <CustomInput v-model="text" />
    <ApartmentsList :items="apartments">
      <template v-slot:title>New title</template>
      <template v-slot:apartment="{ apartment }"
        ><ApartmentsItem
          :key="apartment.id"
          :description="apartment.descr"
          :rating="apartment.rating"
          :price="apartment.price"
          :imgSrc="apartment.imgUrl"
          @click="handleItemClick"
        />
      </template>
    </ApartmentsList>
  </div>
</template>

<script>
import apartments from "./components/apartment/apartments";

import ApartmentsList from "./components/apartment/ApartmentsList.vue";
import ApartmentsItem from "./components/apartment/ApartmentsItem.vue";
import CustomInput from "./components/shared/CustomInput.vue";

export default {
  name: "App",
  components: { ApartmentsList, ApartmentsItem, CustomInput },

  data() {
    return {
      text: "aa",
      apartments,
    };
  },

  methods: {
    handleItemClick() {
      console.log("first", "first");
    },
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
