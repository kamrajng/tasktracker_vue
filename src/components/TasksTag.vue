<template>
    <div :key="task.id" v-for="task in tasks">
        <TaskTag @delete-task="$emit('delete-task', task.id )" :task="task" />
    </div>
</template>

<script>
import TaskTag from './TaskTag';
export default {
    name: 'TasksTag',
    props: {
        tasks: Array,
    },
    components: { TaskTag },
    emits: ['delete-task']
}
</script>

<style>
</style>