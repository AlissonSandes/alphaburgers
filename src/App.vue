<template>
  <v-app>
        <Home />
  </v-app>
</template>

<script>
import Home from './components/Home';

export default {
  name: 'App',

  components: {
    Home,
  },

  data: () => ({
    //
  }),
};
</script>
<style>
body{
  font-family: Zilla Slab;
  font-style: normal;
  font-weight: bold;
  font-size: 22px;
  line-height: 26px;
}
.nopadding{
  margin:0px !important;
  padding: 0px !important;
}
</style>
