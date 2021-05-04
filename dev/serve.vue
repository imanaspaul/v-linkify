<script>
import Vue from 'vue';
import VLinkify from '@/v-linkify.vue';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    VLinkify
  }
});
</script>

<template>
  <div id="app">
    <v-linkify />
  </div>
</template>
