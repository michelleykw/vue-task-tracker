<script>
export default {
  name: 'AddTask',
  data() {
    return {
      text: '',
      day: '',
      reminder: false,
    }
  },
  methods: {
    onSubmit(e) {
      e.preventDefault()
      if (!this.text) {
        alert('Please add a task')
        return
      }
      const newTask = {
        text: this.text,
        day: this.day,
        reminder: this.reminder,
      }
      // reset the values
      this.$emit('add-task', newTask)
      this.text = ''
      this.day = ''
      this.reminder = false
    },
  },
}
</script>

<template>
  <div class="paper">
    <form @submit="onSubmit">
      <div class="form-control">
        <label>Task</label>
        <input type="text" v-model="text" name="text" placeholder="Add Task" />
      </div>
      <div class="form-control">
        <label>Day & Time</label>
        <input
          type="text"
          v-model="day"
          name="day"
          placeholder="Add Day & Time"
        />
      </div>
      <div class="form-control form-control-check">
        <label>Set Reminder</label>
        <input type="checkbox" v-model="reminder" name="reminder" />
      </div>
      <input type="submit" value="Save Task" class="btn btn-block" />
    </form>
  </div>
</template>

<style scoped>
.paper {
  padding: 1.5rem;
  background-color: antiquewhite;
  border-radius: 1rem;
  margin-bottom: 2.5rem;
}
.form-control {
  margin-bottom: 1.5rem;
}
.form-control label {
  display: block;
}
.form-control input {
  width: 100%;
  height: 3.5rem;
  padding: 0.5rem 1rem;
  font-size: 1.25rem;
}
.form-control-check {
  display: flex;
  justify-content: space-between;
}
.form-control-check label {
  flex: 5;
}
.form-control-check input {
  flex: 1;
  height: 1.5rem;
}
</style>