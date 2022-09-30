<template>
    <div class="flex relative pt-10 pb-20 sm:items-center md:w-2/3 mx-auto">
        <div class="h-full w-16 absolute inset-0 flex items-center justify-center">
            <div class="h-full w-1 bg-blue-100 pointer-events-none"></div>
        </div>
        <div
            class="flex-shrink-0 w-16 h-16 rounded-full mt-10 sm:mt-0 inline-flex items-center justify-center bg-blue-600 text-base-100 relative z-10 title-font font-medium text-sm">
            <Icon :name='icon' class="text-white text-3xl" />
        </div>
        <div class="flex-grow md:pl-8 pl-6 flex sm:items-center items-start flex-col sm:flex-row">
            <div class="flex-grow sm:pl-6 mt-6 sm:mt-0">
                <h2 class="font-medium text-black mb-1 text-xl">{{question}}</h2>
                <p class="leading-relaxed">{{answer}}</p>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">

defineProps({
    question: String,
    answer: String,
    icon: String,
})
</script>