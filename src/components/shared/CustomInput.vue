<template>
  <input :value="modelValue" @input="updateValue" class="custom-input" />
</template>

<script>
export default {
  name: "CustomInput",

  props: {
    modelValue: {
      type: String,
      default: "",
    },
  },

  methods: {
    updateValue(event) {
      this.$emit("update:modelValue", event.target.value);
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/scss/variables.scss";

.wrapper-input {
  position: relative;
  display: inline-flex;
}
.custom-input {
  height: 40px;
  width: 100%;
  border: 2px solid $main-color;
  font-size: 18px;
  outline: none;
  line-height: inherit;
  padding: 8px 15px;
  &::placeholder {
    color: inherit;
  }
  &--error {
    border-color: red;
  }
  &__error {
    position: absolute;
    top: 100%;
    right: 0;
    width: 100%;
    font-size: 12px;
    color: red;
    line-height: 1.3;
  }
}
</style>
