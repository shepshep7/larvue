<template>
    <div class="flex min-h-full p-5">
    <!--  SideBar  -->
        <Sidebar :class="{'-ml-[220px]': !sidebarOpened}"/>
    <!--  SideBar  -->
        <div class="flex-1 ">
          <Navbar @toggle-sidebar="toggleSidebar" :class="{'rounded-l-lg ml-4': !sidebarOpened}"></Navbar>
    <!-- Content -->
            <main class="p-6">
                <div class="p-4 rounded bg-white">
                    <router-view></router-view>
                </div>
            </main>
    <!-- Content -->
        </div>
    </div>
</template>

<script setup>
import Sidebar from "./Sidebar.vue";
import Navbar from "./Navbar.vue";
import {ref, onMounted, onUnmounted} from 'vue'

const {title} = defineProps({
    title: String
})

const sidebarOpened = ref(true)

function toggleSidebar() {
    sidebarOpened.value = !sidebarOpened.value
}

onMounted(() => {
    if (window.outerWidth <= 768) {
        sidebarOpened.value = false
    }
    window.addEventListener('resize', handleSidebarOpened)
})

onUnmounted(() => {
    window.removeEventListener('resize', handleSidebarOpened)
})

function handleSidebarOpened() {
    sidebarOpened.value = window.outerWidth > 768
}

</script>

<style scoped>

</style>
