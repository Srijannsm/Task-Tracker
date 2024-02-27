<template>
    <header>
        <h1>{{ title }}</h1>
        <Button @toggle-add-task="$emit('toggle-add-task')" 
        :text="buttonChange ? 'Close':'Add Task' " 
        :color="buttonChange ? 'Red':'Green' "/>
    </header>
</template>

<script>

import Button from './Button'
export default {
    name: 'Header',
    props: {
        title: String,
        buttonChange: Boolean,
    },
    components: {
        Button,
    }
}
</script>

<style scoped>
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}
</style>