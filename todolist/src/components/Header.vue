<template>
    <header>
        <h1>{{ title }}</h1>
        <Button title="Add Task" color="green" />
    </header>
</template>

<script>
import Button from "./Button";

export default {
    name: "Header",
    props: {
        title: {
            type: String,
            default: "Title",
        },
    },
    components: {
        Button,
    },
};
</script>

<style scoped>
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 3rem;
}
</style>
