<template>
<div>
    <h3>List of items: </h3>
  <ul>
    <li v-for="name in names">
      {{ name }}
    </li>
  </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      names: ["Nauman", "Zeeshan", "Subhan"]
    };
  },
  methods: {
    greeting: function() {
      return "wooooooooo, your first practice";
    }
  }
};
</script>

<style scoped>
h3{
    color:goldenrod
}
</style>
