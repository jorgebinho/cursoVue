<template>
  <h2>Propriedades computadas</h2>

  <div>
    {{ fullName }}

    <h3>Todos em aberto</h3>
    <div v-for="todo in notCompletedTodos" :key="todo.id">
        {{ todo.title }}
    </div>

    <h3>Todos realizados</h3>
    <div v-for="todo in completedTodos" :key="todo.id">
        {{ todo.title }}
    </div>

    <h3>Todos</h3>
    <div v-for="todo in todos" :key="todo.id">
        <input v-model="todo.completed" type="checkbox"/>
        {{ todo.title }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user: {
        first_name: "Jorge",
        last_name: "Almeida",
      },
      todos: [
        {
          userId: 1,
          id: 1,
          title: "delectus aut autem",
          completed: false,
        },
        {
          userId: 1,
          id: 2,
          title: "quis ut nam facilis et officia qui",
          completed: false,
        },
        {
          userId: 1,
          id: 3,
          title: "fugiat veniam minus",
          completed: false,
        },
        {
          userId: 1,
          id: 4,
          title: "et porro tempora",
          completed: true,
        },
        {
          userId: 1,
          id: 5,
          title:
            "laboriosam mollitia et enim quasi adipisci quia provident illum",
          completed: false,
        },
      ],
    };
  },
  computed: {
    fullName() {
      return `${this.user.first_name}  ${this.user.last_name}`;
    },
    notCompletedTodos() {
        return this.todos.filter(todo => !todo.completed);
    },
    completedTodos() {
        return this.todos.filter(todo => todo.completed);
    }
  },
};
</script>
