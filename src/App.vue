<template>
  <div id="app">
    <div class="todo-wrapper">
      <div class="todo-container">
<!--        <TodoList/>-->
<!--        <todo-list/>-->
        <todo-list :todos="todos"/>
      </div>
    </div>

  </div>
</template>

<script>

import TodoList from '@/components/TodoList'

export default {
  name: 'app',
  components: {
    TodoList
  },
  data() {
    return {
      todos: [
        {
          _id: '1',
          title: 'Walk the dog',
          description: 'Go to forest near the Zoo'
        },
        {
          _id: '2',
          title: 'Buy a bread',
          description: 'Whole grain bread would be good'
        },
        {
          _id: '3',
          title: 'Learn Programming',
          description: 'Preferable tomorrow'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.todo{
  &-wrapper {
    /* flexible styling*/
    display: flex;
    /*it defines alignment along the main axis*/
    justify-content: center;
    flex-direction: column;
    width: 100%;
    /*height: 2000px;*/
  }
  &-container {
    margin: 0 auto;
    width: 400px;
    min-height: 400px;
    background-color: #ededed;
    border-radius: 5px;
  }
}
</style>
