<template>
<div>
  <ul>
    <li v-for="t in todo" :key="t">
      {{ t }}
    </li>
  </ul>
  <input v-model="newItem" placeholder="Enter the new item to add" />
  <button @click="AddItem()">Add item</button>
</div>
</template>

<script>
export default {
  name: 'ToDoList',
  data () {
    return {
      todo: [],
      newItem: ''
    }
  },
  methods: {
    AddItem () {
      this.todo.push(this.newItem)
      this.newItem = ''
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
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
