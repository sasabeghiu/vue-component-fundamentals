<template>
    <div class="plans">
        <CoffePlan v-for="(plan, index) in plans" :name="plan" :key="index" :isSelected="plan === selectedPlan"
            @selectPlan="selectPlan2"></CoffePlan>
    </div>
</template>

<script>
import CoffePlan from './CoffePlan.vue';

export default {
    components: {
        CoffePlan
    },
    data() {
        return {
            plans: ['The Single', 'The Curious', 'The Addict'],
            selectedPlan: null
        }
    },
    methods: {
        selectPlan2(plan) {
            this.selectedPlan = plan
        }
    }
}
</script>