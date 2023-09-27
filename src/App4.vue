<template>
    <head>
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/semantic-ui/2.4.1/semantic.min.css">
    </head>
    <div id="app" class="ui container">
        <h1>GitHub Profiles</h1>
        <GitHubUserCard v-for="(username, index) in usernames" :key="index" :username="username"></GitHubUserCard>
    </div>
</template>

<script>
import GitHubUserCard from './components/GitHubUserCard.vue';

export default {
    components: {
        GitHubUserCard
    },
    data() {
        return {
            usernames: ['sasabeghiu', 'Paliy0', 'DennisDoksani']
        }
    }
}
</script>