<script>
import Button from './Button.vue'

export default {
    name: 'Header',
    props: {
        title: String,
    },
    components: {
        Button
    }
}
</script>

<template>
    <header>
        <h1>{{ title }}</h1>
        <Button text="Add Task" color="green" />
    </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>