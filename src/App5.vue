<template>
    <head>
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/semantic-ui/2.4.1/semantic.min.css">
    </head>
    <div id="app" class="ui container">
        <h1>Notification Center</h1>
        <NotificationMessage>
            <p>Welcome to Sasha's Airport <b>everyone</b></p>
        </NotificationMessage>

        <NotificationMessage type="error" header="Oh no">
            <p>Your flight has been <b>canceled</b></p>
        </NotificationMessage>

        <NotificationMessage type="success" header="Oh yess">
            <p>Your flight is <b>on time</b></p>
        </NotificationMessage>

        <NotificationMessage type="warning" header="Oh oh">
            <p>Your flight is <b>delayed</b></p>
        </NotificationMessage>
    </div>
</template>

<script>
import NotificationMessage from './components/NotificationMessage.vue';

export default {
    components: {
        NotificationMessage
    }
}
</script>