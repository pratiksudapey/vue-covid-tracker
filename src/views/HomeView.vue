<script setup>
</script>

<template>
<main v-if="!loading">
  <DataTitleVue :text="title" :dataDate="dataDate" />
  <DataBoxesVue :stats="stats" />
</main>
<main class="flex flex-col align-center justify-center text-center" v-else>
<div class="text-gray-500 text-3xl mt-10 mb-6">
  Fetching Data
</div>
<img :src="'/src/assets/hourglass.gif'" class="w-24 m-auto" alt="" />
</main>
</template>
<script>
import DataTitleVue from '../components/DataTitle.vue';
import DataBoxesVue from '../components/DataBoxes.vue';
export default {
  name: 'Home',
  components: {
    DataTitleVue,
    DataBoxesVue
  },
  data() {
    return{
      loading: true,
      title: 'Global',
      dataDate: '',
      stats: {},
      countries: [],
      // loadingImage: require('/src/assets/hourglass.gif'),

    }
  },
  methods: {
    async fetchCovidData(){
      const res = await fetch('https://api.covid19api.com/summary');
      const data = await res.json();
      return data 
    }
  },
  async created(){
    const data = await this.fetchCovidData()
    
    this.dataDate = data.Date
    this.stats = data.Global
    this.countries = data.Countries
    this.loading = false
  },
}
</script>
