<template>
    <div>
        <input type="checkbox" v-model="done">
        <span :class="{ done }">
            <slot></slot>
        </span>
        <slot name="description"></slot>
        <button><slot name="button-text">Highlight</slot></button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            done: false
        }
    }
}
</script>