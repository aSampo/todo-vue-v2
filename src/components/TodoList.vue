<template>
  <div>
    <c-grid m="auto" mt='1%' max-w="600px" w="70%">
      <c-heading  m="auto" size="lg">To-Do App 💚</c-heading>
      <c-input
        @keyup.enter="addTodo"
        v-model="newTodo"
        variant="flushed"
        placeholder="Add task, press enter to save"
      />
      <list></list>
    </c-grid>
  </div>
</template>

<script>
import { CInput, CHeading, CGrid } from '@chakra-ui/vue'
import List from './List'
export default {
  name: 'todo-list',
  components: {
    CInput,
    CHeading,
    CGrid,
    List
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
