<template>
    <div id="ninjas">
        <h3>List of another components</h3>
        <ul>
            <li v-for="ninja in datas" v-on:click="ninja.show = !ninja.show">
                <h2>{{ ninja.name }}</h2>
                <h3 v-show="ninja.show">{{ ninja.speciality }}</h3>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    props:{
        datas:{
            type:Array,
            required:true
        }
    },
    data(){
        return{
          
        }
    }
}
</script>
<style scoped>
#ninjas{
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;
    
   
}
ul{
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
   
}
li{
    flex-grow: 1;
    flex-basis: 300px;
    text-align: center;
    padding: 30px;
    border: 1px solid #222;
    margin: 10px;
}
h3{
    color: lightgreen;
}
</style>