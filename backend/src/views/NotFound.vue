<template>
    <div class="flex justify-center items-center min-h-full min-w-full bg-gray-100">
        <div class="text-indigo-600 text-7xl px-8 pb-7 font-bold border-r">404</div>
        <div class="px-8">
            <h1 class="text-5xl font-bold mb-4">Page Not Found</h1>
            <p class="text-gray-600 mb-2">Please check the url in the address bar and try again</p>
            <div>
                <router-link :to="{name: 'app.dashboard'}" class="group relative flex justify-center rounded-md border border-transparent bg-indigo-600 py-2 px-4 text-sm font-medium text-white hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2">Return to home</router-link>
            </div>
        </div>
    </div>
</template>

<script setup>

</script>

<style scoped>

</style>
