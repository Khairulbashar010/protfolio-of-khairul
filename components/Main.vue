<template>
  <div class="h-[100vh] relative p-10 transform duration-400" :class="dark ? 'bg-black text-white' : 'bg-gray-500'">
	<div class="flex items-center justify-between w-full">
		<Name/>
		<div @click="toggleTheme">
			<Sun v-if="!dark"/>
			<Moon v-else-if="dark"/>
		</div>
    </div>
    <Role/>
  </div>
</template>

<script>
export default {
    data() {
        return {
            dark: false
        };
    },
    methods: {
        toggleTheme() {
            this.dark = !this.dark;
            localStorage.setItem("dark", this.dark);
        }
    },
    mounted() {
        localStorage.getItem("dark") ? this.dark = JSON.parse(localStorage.getItem("dark")) : localStorage.setItem("dark", false);
    },
}
</script>
<style scoped>
body {
  @apply m-10
}
.themeIcon {
  @apply cursor-pointer
}
</style>
