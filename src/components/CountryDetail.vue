<template lang="html">
<div v-if="country">
  <h1>{{country.name}}</h1>
  <p>Capital: {{country.capital}}</p>
  <p>Population: {{country.population}}</p>
  <img :src="country.flag" alt="">
</div>
</template>

<script>
export default {
  name: 'country-selected',
  props: ['country']
}
</script>

<style lang="css" scoped>



img {
  width: 40px;
  height: auto;
}
</style>
