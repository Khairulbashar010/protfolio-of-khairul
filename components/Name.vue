<template>
    <div class="w-full">
        {{name}}
    </div>
</template>
<script>
export default {
    data() {
        return {
            name: ''
        }
    },
    mounted() {
        this.name = process.env.name
    }
}
</script>
<style scoped>
div {
    @apply text-4xl left-10 top-10 transform duration-700
}
</style>