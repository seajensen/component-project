<template>
  <v-app>
    <v-content>
      <layout/>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import Layout from './components/Layout';

export default {
  name: 'App',
  components: {
    HelloWorld,
    Layout,
  },
  data: () => ({
    //
  }),
};
</script>
