<template>
  <div class="todo">
    <div>
      <input type="text" v-model="title">
      <input class="square_btn" type="button" value="追加" @click="addToDo" />
    </div>
    <div class="list">
      <li v-for="todo in todoList" v-bind:key="todo.id">
        {{ todo.title }}
      </li>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ToDo',
  data () {
    return {
      todoList: [
        {
          id: 1,
          title: 'do hogehoge'
        },
        {
          id: 2,
          title: 'do higehige'
        }
      ],
      nextId: 3,
      title: ''
    }
  },
  methods: {
    addToDo: function (event) {
      this.todoList.push({id: this.nextId++, title: this.title})
      this.title = ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
a {
  color: #42b983;
}
div .list {
  padding-top: 10px
}
</style>
