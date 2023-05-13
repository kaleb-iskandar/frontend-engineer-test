<template>
  <div>
    <input class="input" type="text" v-model="searchQuery" placeholder="Search...">
    <ul>
      <li v-for="item  in filteredList" v-bind:key="item">{{ item }}</li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'SearchFilter',
  data () {
    return {
      searchQuery: '',
      list: ['Apple', 'Banana', 'Cherry', 'Durian', 'Eggplant', 'Mango', 'Strawberry', 'Blueberry', 'Raspberry', 'Raspberry1', 'Raspberry2']

    }
  },
  computed: {
    filteredList () {
      return this.list.filter(item => {
        return item.toLowerCase().includes(this.searchQuery.toLowerCase())
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 .5em;
  font-size: 1.5em;
}
.input {
  font-size: 1em;
  padding: .5em;
  border: solid #41b883 .2em;
  border-radius: 25px;
}
</style>
