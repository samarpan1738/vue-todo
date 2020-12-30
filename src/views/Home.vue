<template>
    <div class="home">
        <input-box :val="val" />
        <button @click="addTodo">Add</button>
        <list :todos="todos" />
    </div>
</template>

<script>
// @ is an alias to /src
import InputBox from "@/components/InputBox.vue";
import List from "../components/List";
export default {
    name: "Home",
    components: {
        InputBox,
        List,
    },
    data: () => {
        return { val: "", todos: [] };
    },
    methods: {
        addTodo: function() {
            this.todos.push({ content: this.val, done: false });
            console.log(this.val);
            this.val = "";
        },
    },
    watch: {},
    computed: {},
};
</script>
