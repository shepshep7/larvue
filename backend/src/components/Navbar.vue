<template>
<header class="h-14 shadow bg-white flex justify-between items-center rounded-r-lg">
    <button @click="emit('toggle-sidebar')" class="flex ml-3 w-8 h-8 items-center justify-center text-gray-700 hover:bg-black/10 rounded-lg transition-colors">
        <Bars3Icon class="w-6"/>
    </button>
    <div>

        <Menu as="div" class="relative inline-block text-left mr-3">
            <div>
                <MenuButton class="flex items-center">
                    <img src="https://randomuser.me/api/portraits/men/60.jpg" class="w-8 rounded-full">
                    <p class="ml-2">Chris Dorner</p>
                    <ChevronDownIcon
                        class="ml-2 -mr-1 h-5 w-5 text-indigo-700 hover:text-violet-100"
                        aria-hidden="true"
                    />
                </MenuButton>
            </div>

            <transition
                enter-active-class="transition duration-100 ease-out"
                enter-from-class="transform scale-95 opacity-0"
                enter-to-class="transform scale-100 opacity-100"
                leave-active-class="transition duration-75 ease-in"
                leave-from-class="transform scale-100 opacity-100"
                leave-to-class="transform scale-95 opacity-0"
            >
                <MenuItems
                    class="absolute right-0 mt-2 w-36 origin-top-right divide-y divide-gray-100 rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
                >
                    <div class="px-1 py-1">
                        <MenuItem v-slot="{ active }">
                            <button
                                :class="[
                  active ? 'bg-indigo-500 text-white' : 'text-gray-900',
                  'group flex w-full items-center rounded-md px-2 py-2',
                ]"
                            >
                                <UserIcon
                                    :active="active"
                                    :class="[ active ? 'text-white' : 'text-indigo-500', 'mr-2 h-5 w-5' ]"
                                    aria-hidden="true"
                                />
                                Profile
                            </button>
                        </MenuItem>
                        <MenuItem v-slot="{ active }">
                            <button
                                :class="[
                  active ? 'bg-indigo-500 text-white' : 'text-gray-900',
                  'group flex w-full items-center rounded-md px-2 py-2',
                ]"
                            >
                                <ArrowLeftOnRectangleIcon
                                    :active="active"
                                    :class="[ active ? 'text-white' : 'text-indigo-500', 'mr-2 h-5 w-5' ]"
                                    aria-hidden="true"
                                />
                                Logout
                            </button>
                        </MenuItem>
                    </div>
                </MenuItems>
            </transition>
        </Menu>
    </div>
</header>
</template>

<script setup>
 import {Bars3Icon, UserIcon, ArrowLeftOnRectangleIcon} from '@heroicons/vue/24/outline'
 import { Menu, MenuButton, MenuItems, MenuItem } from '@headlessui/vue'
 import { ChevronDownIcon } from '@heroicons/vue/20/solid'

 const emit = defineEmits(['toggle-sidebar'])

</script>

<style scoped>

</style>
