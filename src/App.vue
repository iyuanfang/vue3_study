<template>
<img alt="Vue logo" src="./assets/logo.png" />
<HelloWorld msg="Hello Vue 3.0 + Vite" />
<p>{{message}}</p>
<input v-model="message"></input><br>

<span v-if="seen">Now you see me</span><br>
<button @click="changeSeen()">change seen</button>

<ol>
    <TodoItem v-for="todo in todos" v-bind:msg="todo.text"></TodoItem>
</ol>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import TodoItem from './components/TodoItem.vue';

export default {
    data() {
        return {
            message: "test",
            seen: true,
            todos: [{
                    text: 'Learn JavaScript'
                },
                {
                    text: 'Learn Vue'
                },
                {
                    text: 'Build something awesome'
                }
            ]
        }
    },
    components: {
        HelloWorld,
        TodoItem
    },
    methods: {
        changeSeen() {
            this.seen = !this.seen;
        }
    }
}
</script>
