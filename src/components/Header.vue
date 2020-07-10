<template>
  <header class="header">
    <h1>ToDo App</h1>
  </header>
  
</template>

<script>
export default {
  name: "Header"
}

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Pattaya&display=swap');
@import url('https://fonts.googleapis.com/css?family=Roboto+Condensed');

  .header {
    font-family: 'Pattaya', sans-serif;
    background: #333;
    color: #fff;
    text-align: center;
    padding: 10px;
    box-shadow: 0px 4px 25px rgba(0, 0, 0,  0.5);
    border-radius: 5px;
  }

  .header a {
    font-family: Roboto Condensed, san-serif;
    color: #fff;
    padding-right: 5px;
    text-decoration: none;
    cursor: "pointer";
  }
</style>
