<template>
    <div id="app">
        <h1>Vue.js Components Fundamentals</h1>
        <ClickCounter></ClickCounter>
        <ClickCounter></ClickCounter>
        <ClickCounter></ClickCounter>
        <ClickCounter></ClickCounter>
    </div>
</template>

<script>
import ClickCounter from './components/ClickCounter.vue';

export default {
    components: {
        ClickCounter
    }
}
</script>