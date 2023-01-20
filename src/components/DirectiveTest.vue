<template>
  <div v-if="isVisible">
    <h3>Directives</h3>
    <ul>
      <template v-for="fruit in fruits">
        <li v-if="fruit === 'kiwi'" :key="fruit">{{ fruit }}</li>
      </template>
    </ul>
    <ul>
      <li v-for="(car, key) in cars" :key="key">
        {{ `${key} - color ${car.color}` }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "DirectiveTest",
  data() {
    return {
      isVisible: true,
      fruits: ["apple", "banana", "cherry", "kiwi"],
      cars: {
        audi: { color: "red" },
        bmw: { color: "green" },
      },
    };
  },
};
</script>

<style lang="scss" scoped></style>
