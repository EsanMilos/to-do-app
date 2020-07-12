<template >
<div id="app">

 <toDoContainer content="to-dos"/>
 
  </div>

</template>

<script>
import ToDoContainer from './components/ToDoContainer.vue'

export default {
  name: 'App',
  components: {
    ToDoContainer,
    
  }, 
}



</script>


<style scoped>

body {
  background-color: red;
}

</style>

