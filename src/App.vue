<template>
  <div>
<!-- Render the TodoList component
     TodoList becomes-->

  <!--We will need to pass data from the main component 
  to the TodoList component. For this, we will use the v-bind 
  directive. The directive takes an argument which is indicated by 
  a colon after the directive name. Our argument will be todos which 
  tells the v-bind directive to bind the element’s todos attribute to 
  the value of the expression todos.-->
    <todo-list v-bind:todos="todos"></todo-list>
  </div>
</template>

<script>
import TodoList from "./components/TodoList";

export default {
  name: "app",
  components: {
    TodoList
  },

  data() {
    return {
      todos: [
        {
          title: "Todo A",
          project: "Project A",
          done: false
        },
        {
          title: "Todo B",
          project: "Project B",
          done: true
        },
        {
          title: "Todo C",
          project: "Project C"
        },
        {
          title: "Todo D",
          project: "Project D",
          done: false
        }
      ]
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
