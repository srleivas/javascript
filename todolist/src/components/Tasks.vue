<template>
    <div class="tasks-container">
        <div v-for="task in tasks" :key="task.id">
            <Task
                @toggle-reminder="$emit('toggle-reminder', task.id)"
                @delete-task="$emit('delete-task', task.id)"
                :task="task"
            />
        </div>
    </div>
</template>

<script>
import Task from "./Task";

export default {
    name: "Tasks",
    props: {
        tasks: Array,
    },
    components: {
        Task,
    },
};
</script>

<style scoped>
.taks-container {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}
</style>
