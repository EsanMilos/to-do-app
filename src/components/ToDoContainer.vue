<template>
<div>
   <vue-particles
    color="#7B1FA2"
    :particleOpacity="0.9"
    :particlesNumber="120"
    shapeType="polygon"
    :particleSize="6"
    linesColor="#f3f2a5"
    :linesWidth="1"
    :lineLinked="true"
    :lineOpacity="0.4"
    :linesDistance="100"
    :moveSpeed="6"
    :hoverEffect="true"
    hoverMode="grab"
    :clickEffect="true"
    clickMode="repulse"
> </vue-particles>
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

#particles-js {
  background-color: #f3f2a5;
 height: 100vh;
}

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
    top: 24%;
    bottom: 5%;
    background: #FFFFFF;
    box-shadow: 0px 5px 35px rgba(0, 0, 0, 0.05);
  }

  .main-box img {
    padding-top: 10%;
    width: 199px;
    height: 199px;
  }

  @media(max-width: 400px), (max-width: 600px) {

.main-box {
    text-align: center;
    margin-top: 20%;
    position: fixed;
    width: 70%;
    max-height: 70%;
    left: 15%;
    right: 35%;
    top: 5%;
  }

.main-box img {
    padding-top: 10%;
    width: 99px;
    height: 99px;
  }

}
</style>