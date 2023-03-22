<template>
    <footer>
      <h2>{{ 'copyRights By 2023'+ " "+title }}</h2>
    </footer>
  </template>
  
  <script>
  export default {
    props:{
        title:{
            type:String
        }
    },
    data() {
      return {
        title: "copyRights By 2023"
      };
    }
  };
  </script>
  
  <style scoped>
  footer {
    background: rgb(17, 17, 17);
    padding: 14px;
  }
  h2 {
    text-align: center;
    color: lightgreen;
  }
  </style>
  