<template>
  <div id="app">
    <h1>COUNTRIES</h1>
    <div>
      <countries-list :countries='countries'></countries-list>
    </div>
  </div>
</template>

<script>
import CountriesList from './components/CountriesList.vue';

export default {
  name: 'App',
  data(){
    return {
      countries: [],
      selectedCountry: null
    };
  },
  components: {
    "countries-list": CountriesList
  },
  mounted(){
    fetch('https://restcountries.eu/rest/v2/all')
    .then(res => res.json())
    .then(countries => this.countries = countries)
  }
}
</script>

<style>
#app {

}
</style>
