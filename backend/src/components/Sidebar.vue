<template>
    <div class="w-[200px] transition-all bg-indigo-700 text-gray-300 py-4 px-2 rounded-l-xl">
        <router-link :to="{name: 'app.dashboard'}" class="flex items-center transition-colors py-1 px-3 rounded hover:bg-black/30">
            <span class="mr-3"><HomeIcon class="w-5"/></span>
            <span class="text-gray-200 font-light">Dashboard</span>
        </router-link>
        <router-link :to="{name: 'app.products'}" class="flex items-center transition-colors py-1 px-3 rounded hover:bg-black/30">
            <span class="mr-3"><ListBulletIcon class="w-5"/></span>
            <span class="text-gray-200 font-light">Products</span>
        </router-link>
        <router-link :to="{name: 'app.dashboard'}" class="flex items-center transition-colors py-1 px-3 rounded hover:bg-black/30">
            <span class="mr-3"><UsersIcon class="w-5"/></span>
            <span class="text-gray-200 font-light">Users</span>
        </router-link>
        <router-link :to="{name: 'app.dashboard'}" class="flex items-center transition-colors py-1 px-3 rounded hover:bg-black/30">
            <span class="mr-3"><ChartBarIcon class="w-5"/></span>
            <span class="text-gray-200 font-light">Reports</span>
        </router-link>
    </div>
</template>

<script setup>
import {HomeIcon, ListBulletIcon, UsersIcon, ChartBarIcon} from '@heroicons/vue/24/outline'

</script>

<style scoped>

</style>
