<template>
<div>
    <div>
      <div>
        <h1>{{ listName }}</h1>
      </div>
    </div>
    <div>
      <create-todo @on-new-todo="addTodo($event)" />
    </div>
    <div>
      <div>
        <ul>
          <todo
            v-for="(todo, index) in todos"
            :key="index"
            :description="todo.description"
            :completed="todo.completed"
            @on-toggle="toggleTodo(todo)"
            @on-delete="deleteTodo(todo)"
          />
        </ul>
      </div>
    </div>
    </div>
  
</template>

<script>
import Todo from "./Todo.vue";
import CreateTodo from "./CreateTodo.vue";


export default {
    props: {
        listName: String,
    },
  data() {
    return {
      todos: [
        { description: "Get some sleep", completed: false },
        { description: "Go for a walk", completed: true },
        { description: "Eat something", completed: false },
      ],
    };
  },
  methods: {
    addTodo(newTodo) {
      this.todos.push({ description: newTodo, completed: false });
    },
    toggleTodo(todo) {
      todo.completed = !todo.completed;
    },
    deleteTodo(deletedTodo) {
      this.todos = this.todos.filter(todo => todo !== deletedTodo);
    },
  },
 components: { Todo, CreateTodo },
}
</script>