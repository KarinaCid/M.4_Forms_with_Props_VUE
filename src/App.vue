<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <h1>Crear nueva tarea</h1>

    <label for="tarea">Tarea</label>
    <input
      type="text"
      id="tarea"
      v-model="newTask"
      placeholder="Ingresa una nueva tarea"
    />
    <button @click="addTask" class="btn-1">Crear</button>
    <HelloWorld msg="Listas" :tasks="tasks"/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      newTask: "",
      tasks: [],
    };
  },
  components: {
    HelloWorld,
  },
  methods: {
    addTask() {
      this.tasks.push(this.newTask);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
