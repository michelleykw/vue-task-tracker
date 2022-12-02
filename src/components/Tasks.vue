<script>
import TaskItem from './TaskItem.vue';

export default {
    name: 'Tasks',
    props: {
        tasks: Array
    },
    components: {
        TaskItem
    },
    emits: ['delete-task', 'toggle-reminder'],
}
</script>

<template>
    <div :key="task.id" v-for="task in tasks">
        <TaskItem
            @toggle-reminder="$emit('toggle-reminder', task.id)"
            @delete-task="$emit('delete-task', task.id)" 
            :task="task" 
        />
    </div>
</template>