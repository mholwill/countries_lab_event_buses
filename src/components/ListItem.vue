<template lang="html">
  <div>
    <li @click="handleClick">{{country.name}}</li>
  </div>
</template>

<script>
import {eventBus} from '../main.js'
export default {
  name: 'list-item',
  props: ['country'],
  methods: {
    handleClick(){
      eventBus.$emit('country-selected',this.country)
    }

  }
}
</script>

<style lang="css" scoped>

li {
  cursor: pointer;
  list-style-type: none;
  border: 1px dotted hotpink;
  margin: 10px;
}

li:hover {
  background-color: blue;
}

</style>
