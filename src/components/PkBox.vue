<template>
<div id="box">
    <h1 id="h1test">---</h1>
    <v-select label="Pokémon 1" :items="pkmonlist">Hi</v-select>
    <v-select label="Pokémon 2"></v-select>
    <v-btn id="match-btn">MATCH</v-btn>
</div>
</template>

<style>
#box {
    width: 500px;
    height: 400px;
    color: black;
    background-color: rgb(255, 255, 255);
    margin: auto;
}
#h1test {
    color: black;
}
#match-btn {
    background-color: red;
    color: white;
    margin-left: 41%;
    margin-right: 41%;
    width: 18%;
}
</style>


<script>
import {pkmon} from '../assets/pkmon.js'

export default {
  data: () => ({
    name: "Sean",
    pkmonlist: [],
  }),
  methods: {
      pkarray: function() {
          for (i = 0; i < pkmon.length; i++) {
            this.pkmonlist.shift(pkmon[i].name);
        }
      }
  },
};
</script>
