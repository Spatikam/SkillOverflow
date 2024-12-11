<script setup>

</script>

<template>
    <div class="nav-bar">
        <button class="nav-button">Coding</button>
        <button class="nav-button">Design</button>
        <button class="nav-button">Video Editing</button>
        <button class="nav-button">Language</button>
        <button class="nav-button" @click="emit_logot_event">Logout</button>
    </div>
</template>

<script>
    export default{
        methods: {
            emit_logot_event(){
                this.$emit('custom-logout-event', 'Continue');
            }
        }
    }
</script>


<style scoped>
    .nav-bar{
        background-color: rgb(1, 1, 1);
        width: 100%;
        height: 7%;
        display: flex;
        justify-content: space-evenly;
        align-items: center;
    }
    .nav-button{
        background-color: rgb(58, 58, 58);
        color: white;
        font-size: 150%;
        font-weight: bold;
        border-radius: 25px;
        width: 10%;
        padding: 5px;
        border: solid;
        border-color: black;
        transition: 300ms;
        cursor: pointer;
    }
    .nav-button:hover{
        border-color: white;
        background-color: white;
        color: black;
    }
</style>