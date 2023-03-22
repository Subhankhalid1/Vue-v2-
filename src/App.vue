<template>
  <div>

    <!-- Pass Data Child to parent through event -->
 <app-header v-bind:title="title" v-on:changedTitle="updatedTitle($event)" ></app-header>

 <Keep-alive>
  <component v-bind:is="component"></component>
 <!-- <app-another1 v-bind:datas="datas"></app-another1>
 <app-another2></app-another2> -->
</Keep-alive>

<button v-on:click="component='app-another1'">Another 1</button>
 <button v-on:click="component='app-another2'">Another 2</button>
 <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

<script>
//  import Custom from "./Custom.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Another1 from "./components/Another1.vue";
import Another2 from "./components/Another2.vue";
export default {
 components:{
 'app-header':Header,
 'app-footer':Footer,
  'app-another1':Another1,
  'app-another2':Another2
 },
 
  data () {
    return {
      component:"app-another2"
      // datas: [
      //           {name: 'NAUMAN', speciality: 'DR', show: false},
      //           {name: 'ZEESHAN', speciality: 'PROJECT MANAGER', show: false},
      //           {name: 'SUBHAN', speciality: 'JAVASCRIPT DEVELOPER', show: false},
      //           {name: 'AHMAD', speciality: 'DEVOPS ENGINEER', show: false},
      //           {name: 'ASAD', speciality: 'REACTJS', show: false},
      //           {name: 'SHAHZRAIZ', speciality: 'Data Diggin', show: false}
      //       ],
      //       title:"VUE FOR THE FIRST TIME"
    }
  },
  methods:{
    updatedTitle:function(ev){

      this.title=ev
      
    }
  }
}
</script>

<style scoped>
body{
    margin: 0;
    font-family: 'Nunito SemiBold';
  
}
</style>
