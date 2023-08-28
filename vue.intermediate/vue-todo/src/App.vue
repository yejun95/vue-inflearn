<template>
  <div id="app">
    <TodoHeader/>
    <TodoInput/>
    <TodoList/>
    <TodoFooter/>
    <!-- <DemoHelper/> -->
  </div>
</template>

<script>
import TodoHeader from './components/TodoHeader.vue';
import TodoInput from './components/TodoInput.vue';
import TodoFooter from './components/TodoFooter.vue';
import TodoList from './components/TodoList.vue';
// import DemoHelper from './components/DemoHelper.vue';

export default {
  data: function() {
    return {
      // todoItems: [],
    }
  },
  methods: {
    // == mutations
    // addOneItem: function(todoItem) {
    //   let obj = {completed: false, item: todoItem};
    //   localStorage.setItem(todoItem ,JSON.stringify(obj));
    //   this.todoItems.push(obj);
    // },
    // removeOneItem: function(todoItem, index) {
    //   localStorage.removeItem(todoItem.item);
    //   this.todoItems.splice(index, 1);
    // },
    // toggleOneItem: function(todoItem, index) {
    //   this.todoItems[index].completed = !this.todoItems[index].completed;
    //   // 로컬 스토리지의 데이터를 갱신
    //   localStorage.removeItem(todoItem.item);
    //   localStorage.setItem(todoItem.item, JSON.stringify(todoItem));
    // },
    // clearAllItems: function() {
    //   localStorage.clear();
    //   state.todoItems = [];
    // }
  },
  
  components: {
    TodoHeader,
    TodoInput,
    TodoList,
    TodoFooter,
    // DemoHelper
  }
}
</script>

<style>
  @import url("https://pro.fontawesome.com/releases/v6.0.0-beta1/css/all.css");

  body {
    text-align: center;
    background-color: #F6F6F6;
    display: flex;
    justify-content: center;
  }
  input {
    border-style: groove;
    width: 200px;
  }
  button {
    border-style: groove;
  }
  .shadow {
    box-shadow: 5px 10px 10px rgba(0,0,0, 0.03);
  }

</style>
