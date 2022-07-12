<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Header1 from './components/Header.vue';

</script>

<template>
<Header1 />
<div class="container">
  <RouterView />
</div>

</template>
<script>
import Header from './components/Header.vue';
export default{
  components: {
    Header
  }
}
</script>

