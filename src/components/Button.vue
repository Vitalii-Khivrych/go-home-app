<template>
  <button v-bind:type="type" class="btn btn--outlined">
    <!-- <button v-bind:type="type" :class="['btn', 'btn--outlined']"> -->
    <!-- <button v-bind:type="type" :class="{ btn: true, 'btn--outlined': outlined }"> -->
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "ButtonVue",
  props: {
    type: {
      type: String,
      default: "button",
    },

    outlined: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="scss" scoped>
.btn {
  display: inline-block;
  font-size: 18px;
  background: orangered;
  color: #000000;
  cursor: pointer;
  min-width: 220px;
  border: 1px solid transparent;
  padding: 8px 15px;

  &--outlined {
    background: none;
    border: 1px solid orangered;
    color: orangered;
  }
}
</style>
