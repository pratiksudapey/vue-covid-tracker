<script setup>
// defineProps({
//   msg: {
//     type: String,
//     required: true
//   }
// })
</script>

<template>
  <header class="text-center bg-blue-800 text-white p-4 mb-10">
    <div class="text-3xl md:text-5xl font-bold mb-3"><i class="fa fa-viruses"></i> Covid-19 Tracker</div>
    <p>API by <a class="text-blue-300" href="https://covid19api.com" target="_blank">covid19api</a></p>
  </header>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
