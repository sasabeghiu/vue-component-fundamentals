<template>
    <div class="ui message" :class="type" v-if="!hidden">
        <i class="close icon" @click="hide"></i>
        <div class="header">
            {{ header }}
        </div>
        <slot></slot>
    </div>
</template>

<script>
export default {
    props: {
        type: { type: String, default: 'info' },
        header: { type: String, default: 'Information' },
    },
    data() {
        return {
            hidden: false
        }
    },
    methods: {
        hide() {
            this.hidden = true
        }
    }
}
</script>