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
    
    top: 0%;
    font-family: 'Pattaya', sans-serif;
    background: #333;
    color: #fff;
    text-align: center;
    padding: 10px;
    box-shadow: 0px 5px 35px rgba(0, 0, 0,  0.5);
    position: fixed;
    width: 100%;
  }

  .header a {
    font-family: Roboto Condensed, san-serif;
    color: #fff;
    padding-right: 5px;
    text-decoration: none;
    cursor: "pointer";
  }
</style>
