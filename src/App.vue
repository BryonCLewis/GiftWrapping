<template>
  <v-app>    
    <v-content>
      <gift-wrap-header></gift-wrap-header>
    </v-content>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';
import GiftWrapHeader from './components/GiftWrapper/Header/GiftWrapHeader.vue';

export default Vue.extend({
  name: 'App',

  components: {
    GiftWrapHeader
  },

  data: () => ({
    //
  }),
});
</script>
