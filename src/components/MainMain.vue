<template>
    <main class="main">
        <div class="create-todo-area">
            <input type="text" placeholder="Adicionar nova tarefa" v-model="newTodoInput">
            <button @click="newTodo">Adicionar</button>
        </div>

        <UiAlert />

        <div class="todo-list">
            <div class="list-item" v-for="todo in todos" :key="todo">
                <input class="check" type="checkbox" v-model="todo.completed"
                    :id="todo.id">
                <label class="text" :for="todo.id">{{ todo.name }}</label>
            </div>
        </div>

    </main>
</template>

<script>

import UiAlert from './ui/UiAlert.vue';

export default {
    name: "MainMain",

    components: { UiAlert },

    data() {
        return {
            newTodoInput: "",
            todos: [],
        };
    },

    watch: {
        todos: {
            handler() {
                console.log("\n\n", this.todos, "\n\n");
            },
            deep: true
        },
    },

    methods: {
        newTodo() {
            if (this.newTodoInput.length > 0) {
                this.todos.push({
                    id: (new Date()).getTime(),
                    name: this.newTodoInput,
                    completed: false
                });
                this.newTodoInput = "";
                console.clear();
                console.log("Nova tarefa adicionada!");
            }
            else {
                console.log("Preencha o campo!");
            }
        },
    },
}

</script>

<style>
.main {
    margin-top: 20px;
}

.create-todo-area {
    display: flex;
}

.create-todo-area>input {
    width: 100%;
    padding-top: 12px;
    padding-bottom: 12px;
    border: 1px solid rgb(229, 228, 228);
    font-size: 1rem;
    font-weight: 500;
    text-align: center;
}

.create-todo-area>input:focus {
    outline: none;
    box-shadow: 0 0 6px -1px #41B883;
}

.create-todo-area>button {
    background-color: #41B883;
    border: 0;
    color: #f2f2f2;
    padding-left: 12px;
    padding-right: 12px;
    cursor: pointer;
}

.todo-list {
    margin-top: 20px;
    margin-bottom: 20px;
}

.todo-list>.list-item {
    display: flex;
    align-items: center;
    background-color: transparent;
    padding: 8px 20px;
    margin-bottom: 1px;
    text-align: left;
}

.todo-list>.list-item:hover {
    background-color: #41B883;
    color: #f2f2f2;
    cursor: pointer;
}

.todo-list>.list-item>.text {
    font-weight: 600;
    margin-left: 6px;
    color: rgb(60, 60, 60);
}
</style>
