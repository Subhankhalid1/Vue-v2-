<template>
  <header>
    <h2 v-on:click="changedTitle">{{ title ?title:"Hello Dummy Data"}}</h2>
  </header>
</template>

<script>
export default {
  props: {
    title: {
      type: String
    }
  },
  data() {
    return {
      //   title: "Hell from Subhan"
    };
  },
  methods: {
    changedTitle: function() {
      this.$emit('changedTitle', 'Updated FROM CHILD TO PARENT' )
    }
  }
};
</script>

<style scoped>
header {
  background: lightgreen;
  padding: 20px;
}
h2 {
  text-align: center;
  color: black;
}
</style>
