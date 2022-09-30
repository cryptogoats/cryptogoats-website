<template>
    <header class="bg-white sticky z-50 top-0 shadow-xl">
    <nav class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8" aria-label="Top">
      <div class="flex w-full items-center justify-between border-b border-blue-700 py-6 lg:border-none">
        <div class="flex items-center">
          <a href="/">
            <span class="sr-only">CG</span>
            <img class="h-10 w-auto" src="/favicon.ico" alt="" />
          </a>
          <div class="ml-10 hidden space-x-8 lg:block">
            <a v-for="link in navigation" :key="link.name" :href="link.href" class="text-base font-medium text-black hover:text-blue-500">{{ link.name }}</a>
          </div>
        </div>
        <div class="ml-10 space-x-4">
          <a href="/pricing" class="inline-block rounded-md border border-transparent bg-blue-500 py-2 px-4 text-base font-medium text-white hover:bg-opacity-75">Join Now!</a>
        </div>
      </div>
      <div class="flex flex-wrap justify-center space-x-6 py-4 lg:hidden">
        <a v-for="link in navigation" :key="link.name" :href="link.href" class="text-base font-medium text-black hover:text-blue-500">{{ link.name }}</a>
      </div>
    </nav>
  </header>
</template>

<script setup lang="ts">
  
const navigation = [ 
  { name: 'Home', href: '/' },
  { name: 'Pricing', href: '/pricing' },
  { name: 'FAQ', href: '/faq' },
]
 
</script>