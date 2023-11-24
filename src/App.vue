<script>
  export default{
    data(){
      return{
        name: '',
        list: [],
      }
    },
    methods:{
      sayHello(){
        this.list.push(this.name);
        console.log(this.list);
      }
    }
  }
</script>

<template>
   
    <h1>Список задач {{ name==''?'_______________':name }}</h1>
    <p class="dun">Список текущих задач</p>
    <input class="in" type="text" v-model="name"><br>
    <button v-if="name==''" disabled>Введите задачу</button>
    <button v-else @click="sayHello()">Добавить в список</button>
    <h3>Задача</h3>
    <ul>
      <li v-for="item in list">
      {{ 
        item
         }}</li>
    </ul>
</template>
<style scoped>

</style>