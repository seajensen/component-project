<template>
<body>
<div id="right-side">
    <div id="header-div">
        <img id="icon" src="../assets/pokeball.png">
        <h1>PokéMatch</h1>
    </div>
    <v-content>
        <PkBox/>
    </v-content>
</div>
</body>
</template>

<style>
@import url('https://fonts.googleapis.com/css?family=Bowlby+One&display=swap');

body {
    background-color: white;
    height: 100%;
}
#header-div {
    display: flex;
}
h1 {
    color: white;
    font-family: 'Bowlby One', cursive;
    font-size: 60pt;
    text-align: center;
    margin: auto;
    margin-top: -1px;
    padding-top: 40px;
}
#right-side {
    background-color: red;
    height: 100%;
    margin-left: 16%;
}
#icon {
    width: 200px;
    margin-left: -100px;
}
</style>


<script>
import PkBox from './PkBox';

export default {
  data: () => ({
    name: "Sean",
  }),
  components: {
      PkBox,
  }
};
</script>
