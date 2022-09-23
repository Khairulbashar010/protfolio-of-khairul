<template>
    <div class="w-full">
        <span class="roleName">{{role}}</span> <div class="techStack">{{techStack}}</div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            role: '',
            techStack: '',
        }
    },
    mounted() {
        this.role = process.env.role
        this.techStack = process.env.techStack
    }
}
</script>
<style scoped>
.roleName {
    @apply font-mono text-sm transform duration-[1200ms]
}
.techStack {
    @apply font-mono text-xs transform duration-[1500ms] max-w-[80%]
}
</style>