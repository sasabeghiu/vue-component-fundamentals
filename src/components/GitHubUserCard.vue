<template>
    <div class="ui card">
        <div class="image">
            <img :src="user.avatar_url">
        </div>
        <div class="content">
            <a :href="`https://github.com/${username}`" class="header">{{ user.name }}</a>
            <div class="meta">
                <span class="date">Joined in {{ formatDate(user.created_at) }}</span>
            </div>
            <div class="description">
                {{ user.bio }}
            </div>
        </div>
        <div class="extra content">
            <a :href="`https://github.com/${username}?tab=followers`">
                <i class="user icon"></i>
                {{ user.followers }} Friends
            </a>
        </div>
    </div>
</template>

<script>
import axios from 'axios';

export default {
    props: {
        username: { type: String, required: true }
    },
    data() {
        return {
            user: {}
        }
    },
    async created() {
        const response = await axios.get(`https://api.github.com/users/${this.username}`)
        this.user = response.data
    },
    methods: {
        formatDate(dateString) {
            const options = { year: 'numeric', month: 'long', day: 'numeric', hour: 'numeric', minute: 'numeric' };
            return new Date(dateString).toLocaleDateString(undefined, options);
        }
    }
}
</script>