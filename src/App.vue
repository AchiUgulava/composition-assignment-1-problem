<script setup>
import { ref, reactive } from 'vue';
import Options from "./Options.vue";

const goal = reactive({ title: 'some goal', body: "this is my goal" });
const toggle = ref(true);

const handleToggle = () => {
  toggle.value = !toggle.value
  console.log(toggle.value)
};

</script>

<template>
  <div class="composition">

    <h2>My Course Goal with Composition API</h2>
    <!-- Task 1: Output your main course goal with help of the composition API -->
    <!-- Don't hardcode it into the template, instead hardcode it into the JS code -->
    <div v-show="toggle" class="goal">
      <h3>{{ goal.title }}</h3>
      <h2>{{ goal.body }}</h2>
    </div>
    <!-- Task 2: Toggle (show/ hide) the goal with help of the button  -->
    <button @click="handleToggle">Toggle Goal</button>
    <!-- Task 3: Manage data in three ways -->
    <!-- => Separate refs -->
    <!-- => Ref Object -->
    <!-- => Reactive Object -->
    <!-- Task 4: Also solve the assignment with the Options API -->
  </div>
  <Options />
</template>


<style>
html {
  font-family: sans-serif;
}

body {
  margin: 3rem;
  text-align: center;
}
.composition{
    background-color: rgb(0, 255, 0);
    padding: 30px;
    margin: 20px 0;
    border-radius: 20px;
}
.options{
    background-color: darkgreen;
    padding: 30px;
    margin: 20px 0;
    border-radius: 20px;
}
.goal{
    background-color: azure;
    border-radius: 10px;
    padding:3px 0 ;
    text-align: center;
}
button {
  padding: 10px;
  background-color: cornsilk;
  border-radius: 5px;
  margin-top: 10px;
}

</style>