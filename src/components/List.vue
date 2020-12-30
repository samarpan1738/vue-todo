<template>
    <ul>
        <li v-for="(todo, idx) in todos" :key="idx">{{ todo.content }}</li>
    </ul>
</template>
<script>
export default {
    name: "List",
    props: ["todos"],
};
</script>
<style scoped></style>
