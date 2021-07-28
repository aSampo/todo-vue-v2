<template>
  <div>
    <c-stack m="20px" :spacing="5">
      <task-card/>
    </c-stack>
  </div>
</template>

<script>
import { CStack } from '@chakra-ui/vue'
import TaskCard from './TaskCard'

export default {
  name: 'list',
  components: {
    CStack,
    TaskCard
  },
  data () {
    return {
      newTodo: '',
      todos: [
        {
          id: 1,
          title: 'Tarea 1',
          completed: false,
          editing: false
        }
      ]
    }
  },
  methods: {
    addTodo () {
      console.log(this.newTodo)
      //   this.todos.push({
      //     id: this.todos[this.todos.length - 1].id + 1,
      //     title: this.newTodo,
      //     completed: false
      //   })
      //   this.newTodo = ''
    }
  }
}
</script>

<style></style>
