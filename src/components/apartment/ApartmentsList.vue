<template>
  <Container>
    <slot name="title"></slot>
    <ul class="apartments-list">
      <template v-for="apartment in items">
        <slot v-bind:apartment="apartment" name="apartment"></slot>
      </template>
    </ul>
  </Container>
</template>

<script>
import Container from "../shared/Container.vue";

export default {
  name: "ApartmentsList",
  components: {
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
