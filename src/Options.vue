<script>
export default{
    data(){
        return {
            goal:"this is my goal with options api",
            toggle:true
        }
    },
    methods:{

        handleToggle(){
            this.toggle = !this.toggle
            console.log(this.toggle)
        }
    }
}
    
</script>

<template>
    <div class="options">
        <h2>My Course Goal with Options API</h2>
        <!-- Task 1: Output your main course goal with help of the composition API -->
        <!-- Don't hardcode it into the template, instead hardcode it into the JS code -->
        <div v-show="toggle" class="goal">
            <h3>{{ goal}}</h3>
        </div>
        <!-- Task 2: Toggle (show/ hide) the goal with help of the button  -->
        <button @click="handleToggle">Toggle Goal</button>
        <!-- Task 4: Also solve the assignment with the Options API -->
    </div>
    </template>