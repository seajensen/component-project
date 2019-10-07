<template>
  <v-app>
    <v-content>
      <layout :pkmon="pkmon"/>
    </v-content>
  </v-app>
</template>

<script>
import layout from './components/Layout';
import { pkmon } from './assets/pkmon.js'

console.log(pkmon.name)

export default {
  name: 'App',
  components: {
    layout,
  },
  data: () => {
    return {
      pkmon: pkmon,
    }
  },
};
</script>
