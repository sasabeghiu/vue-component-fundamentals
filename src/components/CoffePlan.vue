<template>
    <div class="plan" :class="{ 'active-plan': isSelected }" @click="selectPlan">
        <div class="description">
            <span class="title">
                {{ name }}
            </span>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        name: { type: String, required: true },
        isSelected: { type: Boolean, default: false }
    },
    methods: {
        selectPlan() {
            this.$emit('selectPlan', this.name)
        }
    }
};
</script>