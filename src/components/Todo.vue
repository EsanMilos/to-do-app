<template>
  <li>
    <a
      title="delete if done"
      :class="{ completed }"
      @click="$emit('on-toggle')"
    >
      <span>{{ description }}</span>
    </a>
    
    <button @click="$emit('on-delete')">
      X
    </button>
  </li>
</template>

<script>
export default {
  props: {
    description: String,
    completed: Boolean
  },
};
</script>

<style scoped>
.completed {
  text-decoration: line-through;
  background-color: #f3f2a5;
}

li {
  padding: 5%;
  margin-right: 10%;
  justify-content: center;
  position: relative;
  transition-delay: 3s;
  background-color: rgb(216, 209, 209);
  overflow: auto;
  margin: right;
  margin-top: 5px;
    list-style-type: none;
    padding: 2px;
    border-radius: 10%;
    border: 3px solid #333;
    max-width: 500px;
    box-shadow: 0px 4px 25px rgba(0, 0, 0, 0.05);
}

li a {
  float: left;
  padding-right: 7%;
  padding-left: 7%;
  border-radius: 10%;
  border: 1px solid gray;
  background-color: rgb(226, 221, 221);
  cursor: pointer;
  margin-top: 1px;
  padding: 0.2%;
  box-shadow: 0px 4px 25px rgba(0, 0, 0, 0.03);
  overflow: auto;
}

li button {
  font-weight: bold;
  float: right;
  margin-top: 1px;
  margin-left: 2%;
  border-radius: 19%;
  border: 2px solid rgb(247, 58, 58);
  background-color: rgb(228, 79, 79);
  box-shadow: 0px 4px 25px rgba(0, 0, 0, 0.03);
  cursor: pointer;
}


li button:hover {
border-color: black;
}

 @media(max-width: 400px), (max-width: 600px) {
   li {
     position: relative;
     max-width: 200px;
   }
 }

</style>