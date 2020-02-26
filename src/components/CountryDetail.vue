<template lang="html">
<div v-if="country">
  <div class="item">
    <h1>{{country.name}}</h1>
    <p>Capital: {{country.capital}}</p>
    <p>Population: {{country.population}}</p>
    <img :src="country.flag" alt="">
  </div>
</div>
</template>

<script>
export default {
  name: 'country-selected',
  props: ['country']
}
</script>

<style lang="css" scoped>

.item {
  border: solid 2px black;
  position: fixed;
  padding: 40px;
  background-color: white;
}

img {
  width: 40px;
  height: auto;
}
</style>
