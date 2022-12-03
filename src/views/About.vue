<script>
export default {
  name: 'About'  
}

</script>
<template>
  <h1>About</h1>
  <p>A task tracker with simple interface, implemented with Vue and a fake API with JSON Server.</p>
  <br>
  <h2>Features include:</h2>
  <ol>
    <li>Add tasks (Name, Day & Reminder)</li>
    <li>Highlight important tasks by double clicking</li>
    <li>Delete tasks</li>
  </ol>
</template>

<style scoped>
  ol {
    padding-left: 1rem
  }
</style>