<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <br><br>
  <Dashboard :text="name"/>
  <br><br>
  <input type="text" v-model="name">
  <br><br>
  <button ref='button' @click="changeName">Click</button>
  <br><br>
  <EventButton @buttonClicked="eventAction"/>
</template>

<script setup >
import {ref, onMounted, onUpdated} from 'vue'
import Dashboard from './components/DashBoard'
import EventButton from './components/EventsButton'

let name = ref(null)

const changeName = () => {
  console.log(name.value)
}

const eventAction = () => {
  console.log('eventAction')
}

onMounted(() => {
  console.log('Mounted')
})

onUpdated(()=>{
  console.log('Updated')
})

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
