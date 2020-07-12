<template>
  <form  @submit.prevent="addTodo()">
    <input
      v-model="newTodo"
      type="text"
      placeholder="Create..."
    />
    <button @click="addTodo()">Add</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      newTodo: ""
    };
  },
  methods: {
    addTodo() {
      if (this.newTodo.length > 0) {
        this.$emit("on-new-todo", this.newTodo);
      }
      this.newTodo = "";
    }
  }
};
</script>

<style scoped>


input {
    max-width: 125px;
    margin-bottom: 20%;
  }

  button {
    background-color: #f3f2a5;
    border-width: 1px;
    padding: 2%, 2%, 2%, 2%;
    font-size: 10px;
    cursor: pointer;
    border-radius: 10%;
    max-width: 30px;
    max-height: 20px;
    margin-bottom: 20%;
  }

  button:hover {
    background-color: indigo;
    color: #ffffff;
  }


@media(max-width: 400px), (max-width: 600px) {
  input {
    max-width: 125px;
  }

  button {
    max-width: 40px;
  }
}
</style>