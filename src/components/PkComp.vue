<template>
<div>
    <div style="display: flex;">
        <img :src="pkmon.sprites.front_default" :id="pkmon.name">
        <v-btn style="background-color: red; color: white; margin: auto; width: 120px;"
        @click="pkmonInfo(pkmon.height, pkmon.weight, pkmon.types)"
        >{{ pkmon.name }}</v-btn>
    </div>
    <div style="background-color: rgb(221, 221, 221);" v-if="infoToggle">
        <p>Type(s): {{pkmonType}}</p>
        <v-divider></v-divider>
        <p>Height: {{pkmonHeight}}</p>
        <v-divider></v-divider>
        <p>Weight: {{pkmonWeight}}</p>
    </div>
</div>
</template>


<script>

export default {
  props: {
      pkmon: {
          type: Object,
      },
  },
  methods: {
        pkmonInfo(a, b, c) {
          if(this.infoToggle == false) {
            this.pkmonHeight = a;
            this.pkmonWeight = b;
            if(c.length > 1)
                {
                    this.pkmonType = c[0].type.name + "/" + c[1].type.name;
                } else {
                    this.pkmonType = c[0].type.name;
                }
            this.infoToggle = true;
          } else if(this.infoToggle == true) {
            this.infoToggle = false;
          }

      }
  },
  data: () => ({
    pkmonType: null,
    pkmonHeight: null,
    pkmonWeight: null,
    infoToggle: false,
  })
};
</script>


<style>

</style>
