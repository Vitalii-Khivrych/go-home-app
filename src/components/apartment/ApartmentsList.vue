<template>
  <Container>
    <div class="apartments-list">
      <ApartmentsItem
        v-for="{ id, descr, rating, price, imgUrl } in items"
        :key="id"
        :description="descr"
        :rating="rating"
        :price="price"
        :imgSrc="imgUrl"
      /></div
  ></Container>
</template>

<script>
import Container from "../shared/Container.vue";
import ApartmentsItem from "./ApartmentsItem.vue";

export default {
  name: "ApartmentsList",
  components: {
    ApartmentsItem,
    Container,
  },

  props: {
    items: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style lang="scss" scoped>
.apartments-list {
  display: flex;
  flex-wrap: wrap;
  margin-left: -15px;
  margin-right: -15px;
}
</style>
