<template>
<div>
<Header/>
    <div class="main-box">
      <img src="../assets/logo.png">
<TodoList />
    </div>
    </div>
</template>

<script>
import TodoList from "./TodoList.vue"
import Header from "./Header.vue"

export default {
    props: {
        content: String,
    },

    components: {
      TodoList,
      Header
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Roboto+Condensed');

.main-box {
    font-family: Roboto Condensed, san-serif;
    color: rgb(32, 32, 32);
    border-radius: 3%;
    overflow: auto;
    text-align: center;
    position: absolute;
    display: inline-block;
    min-width: 40%;
    max-height: 90%;
    left: 29%;
    right: 50%;
    top: 19%;
    bottom: 5%;
    background: #FFFFFF;
    box-shadow: 0px 4px 25px rgba(0, 0, 0, 0.05);
  }

  .main-box img {
    padding-top: 10%;
    width: 199px;
    height: 199px;
  }

  @media(max-width: 400px), (max-width: 600px) {

.main-box {
    text-align: center;
    margin-top: 34%;
    overflow: auto;
    text-align: center;
    position: fixed;
    display: inline-block;
    width: 70%;
    max-height: 70%;
    left: 15%;
    right: 35%;
    top: 5%;
    bottom: 5%;
    background: #FFFFFF;
    box-shadow: 0px 4px 25px rgba(0, 0, 0, 0.05);
  }

.main-box img {
    padding-top: 10%;
    width: 99px;
    height: 99px;
  }

}
</style>