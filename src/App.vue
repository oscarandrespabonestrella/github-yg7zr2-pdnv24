<script lang="ts">
import { defineComponent, ref } from 'vue'
import Sidebar from './partials/Sidebar.vue'
import Header from './partials/Header.vue'

export default defineComponent({
    components: {
        Sidebar,
        Header,
    },
    setup() {
        const sidebarOpen = ref(true)
        return {
            sidebarOpen,
        }
    },
})
</script>

<template>
    <div class="flex h-screen overflow-hidden">
        <!-- Sidebar -->
        <Sidebar
            :sidebarOpen="sidebarOpen"
            @close-sidebar="sidebarOpen = false"
        />

        <!-- Content area -->
        <div
            class="relative flex flex-col flex-1 overflow-y-auto overflow-x-hidden"
        >
            <!-- Site header -->
            <Header
                :sidebarOpen="sidebarOpen"
                @toggle-sidebar="sidebarOpen = !sidebarOpen"
            />

            <main>
                <div class="px-4 sm:px-6 lg:px-8 py-8 w-full max-w-9xl mx-auto">
                    <div class="grid">
                        <router-view></router-view>
                    </div>
                </div>
            </main>
        </div>
    </div>
</template>

<style></style>
