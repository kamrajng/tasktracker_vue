<template>
  <div class="container">
    <TopText title="Task Tracker" />
    <TasksTag @delete-task="deleteTask" :tasks="tasks" />
  </div>
</template>

<script>
import TopText from './components/TopText';
import TasksTag from './components/TasksTag.vue';

export default {
  name: "App",
  components: { TopText, TasksTag },
  data() {
    return {
      tasks: [],
    }
  },
  methods: {
    deleteTask(id) {
      this.tasks = this.tasks.filter ((task) => task.id !== id)
    }
  },
  created() {
    this.tasks = [
      {
        id: 1,
        text: 'Docto',
        day: 'March 1st at 2:30pm',
        reminder: true,
      },
      {
        id: 2,
        text: 'Docntment',
        day: 'March 1st at 2:30pm',
        reminder: true,
      },
      {
        id: 3,
        text: 'Appointment',
        day: 'March 1st at 2:30pm',
        reminder: false,
      },
      {
        id: 4,
        text: 'Doctor',
        day: 'March 1st at 2:30pm',
        reminder: true,
      },
      {
        id: 5,
        text: 'Doctment',
        day: 'March 1st at 2:30pm',
        reminder: true,
      },
      {
        id: 6,
        text: 'pointment',
        day: 'March 1st at 2:30pm',
        reminder: false,
      },
      {
        id: 7,
        text: 'Appointment',
        day: 'March 1st at 2:30pm',
        reminder: true,
      },
      {
        id: 8,
        text: 'Doctment',
        day: 'March 1st at 2:30pm',
        reminder: false,
      },
    ]
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Poppins', sans-serif;
}

.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}

.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}

.btn:focus {
  outline: none;
}

.btn:active {
  transform: scale(0.98);
}

.btn-block {
  display: block;
  width: 100%;
}
</style> 
