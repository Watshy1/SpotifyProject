<script setup lang="ts">

import { RouterLink } from 'vue-router';

</script>

<template>
    <nav class="flex items-center justify-between flex-wrap p-6 bg-dark">
        <div class="flex items-center flex-shrink-0 text-white mr-6">
            <RouterLink to="/" class="font-semibold text-xl tracking-tight">Spotify</RouterLink>
        </div>
        <div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto">
            <div class="text-sm lg:flex-grow">
                <RouterLink to="/albums" class="block mt-4 lg:inline-block lg:mt-0 w-16 text-white hover:font-bold">
                    Albums
                </RouterLink>
            </div>
            <div>
                <a href="/login"
                    class="inline-block text-sm px-4 py-2 leading-none border rounded text-white border-white hover:border-transparent hover:text-teal-500 hover:bg-white mt-4 lg:mt-0">
                    Login
                </a>
            </div>
        </div>
    </nav>
    <div class="flex-grow overflow-y-auto bg-primary">
        <router-view :key="$route.fullPath"></router-view>
    </div>
</template>