<template>
<!-- Javascript expressions in Vue are enclosed in double curly brackets --> 
    <div>
    
    <p> Completed Tasks: {{todos.filter(todo => {return todo.done === true }).length}} </p>
    <p> Pending Tasks: {{todos.filter(todo => {return todo.done === true}).length}} </p>

    <div class="ui centered card" v-for="(todo) in todos" :key="todo">
        <div class="content"> 
            <div class="ui sub header">
                {{ todo.title }} 
            </div>
            <div class="meta"> 
            </div> 
            {{ todo.project}}
        </div>
    <div class="content"> 
    <span class="right floated edit icon"> 
        <i class="edit icon"></i>
        </span> 
            </div> 
    </div>
    </div>

</template>


<!-- We will need to supply data to the main component 
that will be used to display the list of todos. Our todos 
will have three properties; The title, project and done(to 
indicate if the todo is complete or not). Components avail
data to their respective templates using a data function. 
This function returns an object with the properties intended 
for the template. Let's add some data to our component. --> 



<!-- The todos will now be available in the TodoList component as todos.
We will have to modify our TodoList component to access this data. 
The TodoList component has to declare the properties it will accept 
when using it. We do this by adding a property to the component class. --> 

<script type ="text/javascript">
export default {
  props: ["todos"]
};
</script>

<style>
</style>


