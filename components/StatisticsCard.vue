<template>
    <div class="p-4 md:w-1/4 sm:w-1/2 w-full">
        <div class="px-4 py-6 rounded-lg bg-white shadow-xl">
            <Icon :name='icon' class="text-blue-600 text-5xl text-center w-full mb-4" />
            <h2 class="font-medium text-3xl text-gray-900">{{content}}</h2>
            <p class="leading-relaxed">{{title}}</p>
        </div>
    </div>
</template>

<script setup lang="ts">

defineProps({
    title: String,
    content: String,
    icon: String
})
</script>