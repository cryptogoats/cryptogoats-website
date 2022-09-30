<!-- This example requires Tailwind CSS v2.0+ -->
<template>
  <div class="bg-gray-50 pb-36">
    <div class="relative bg-blue-600">
      <!-- Overlapping background -->
      <div aria-hidden="true" class="absolute bottom-0 hidden h-6 w-full bg-gray-50 lg:block" />

      <div class="relative mx-auto max-w-2xl px-4 pt-16 text-center sm:px-6 sm:pt-32 lg:max-w-7xl lg:px-8">
        <h1 class="text-4xl font-bold tracking-tight text-white sm:text-6xl" data-aos="fade-down">
          <span class="block lg:inline">Membership </span>
          <span class="block lg:inline">Options</span>
        </h1>
        <p class="mt-4 text-xl text-blue-100" data-aos="fade-down" data-aos-delay="200">Make the perfect choice for
          participating in our community</p>
      </div>

      <h2 class="sr-only">Membership Options</h2>

      <!-- Toggle -->
      <div class="relative mt-12 flex justify-center sm:mt-16">
        <div class="flex rounded-lg bg-blue-700 p-0.5">
          <button v-for='optionButton, index in optionButtons' type="button"
            class="relative ml-0.5 whitespace-nowrap rounded-md border border-transparent py-2 px-6 text-sm font-medium focus:z-10 focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-blue-700"
            :class=' tabIndex == index  ? "text-blue-600 bg-white hover:bg-white": "text-blue-200 hover:bg-blue-800"'
            v-on:click='changeIndex(index)'>{{optionButton}}</button>
        </div>
      </div>

      <!-- Cards -->
      <div class="relative mx-auto mt-8 max-w-2xl px-4 pb-8 sm:mt-12 sm:px-6 lg:max-w-7xl lg:px-8 lg:pb-0">
        <!-- Decorative background -->
        <div aria-hidden="true"
          class="absolute inset-0 top-4 bottom-6 left-8 right-8 hidden rounded-tl-lg rounded-tr-lg bg-blue-700 lg:block" />

        <div class="relative space-y-6 lg:grid lg:grid-cols-3 lg:space-y-0">
          <div v-for="plan, index in plans" :key="plan.title"
            :class="[plan.featured ? 'bg-white ring-2 ring-blue-700 shadow-md' : 'bg-blue-700 lg:bg-transparent', 'pt-6 px-6 pb-3 rounded-lg lg:px-8 lg:pt-12']"
            data-aos="flip-up" :data-aos-delay='index*100'>
            <div>
              <h3 :class="[plan.featured ? 'text-blue-600' : 'text-white', 'text-base font-semibold']">{{ plan.title }}
              </h3>
              <div
                class="flex flex-col items-start sm:flex-row sm:items-center sm:justify-between lg:flex-col lg:items-start">
                <div class="mt-3 flex items-center">
                  <p :class="[plan.featured ? 'text-blue-600' : 'text-white', 'text-4xl font-bold tracking-tight']">£{{
                  plan.price[tabIndex] }}</p>
                  <div class="ml-4">
                    <p :class="[plan.featured ? 'text-gray-700' : 'text-white', 'text-sm']">GBP / {{ tabIndex == 0
                    ? "month" : "once"}}</p>
                  </div>
                </div>
                <a href="https://upgrade.chat/crypto-goats"
                  :class="[plan.featured ? 'bg-blue-600 text-white hover:bg-blue-700' : 'bg-white text-blue-600 hover:bg-blue-50', 'mt-6 w-full inline-block py-2 px-8 border border-transparent rounded-md shadow-sm text-center text-sm font-medium sm:mt-0 sm:w-auto lg:mt-6 lg:w-full']">Join
                  Now!</a>
              </div>
            </div>
            <h4 class="sr-only">Features</h4>
            <ul role="list" class="pb-8"
              :class="[plan.featured ? 'border-gray-200 divide-gray-200' : 'border-blue-500 divide-blue-500 divide-opacity-75', 'mt-7 border-t divide-y lg:border-t-0']">
              <li v-for="mainFeature in plan.mainFeatures" :key="mainFeature.id" class="flex items-center py-3">
                <Icon name="mdi:check"
                  :class="[plan.featured ? 'text-green-400' : 'text-blue-200', 'w-5 h-5 flex-shrink-0']"
                  aria-hidden="true" />
                <span :class="[plan.featured ? 'text-gray-600' : 'text-white', 'ml-3 text-sm font-medium']">{{
                mainFeature.value }}</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>


    <div class="relative my-36">
      <div class="absolute h-1/2" />
      <div class="relative mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
        <div class="mx-auto max-w-lg overflow-hidden rounded-lg shadow-lg lg:flex lg:max-w-none">
          <div class="flex-1 bg-white px-6 py-8 lg:p-12">
            <h3 class="text-2xl font-bold text-gray-900 sm:text-3xl sm:tracking-tight">Trading View Indicator</h3>
            <p class="mt-6 text-base text-gray-500">The CryptoGoats idicator will help you make better trading
              decisions!</p>
            <div class="mt-8">
              <div class="flex items-center">
                <h4 class="flex-shrink-0 bg-white pr-4 text-base font-semibold text-blue-600">Included Features</h4>
                <div class="flex-1 border-t-2 border-gray-200" />
              </div>
              <ul role="list" class="mt-8 space-y-5 lg:grid lg:grid-cols-2 lg:gap-x-8 lg:gap-y-5 lg:space-y-0">
                <li v-for="feature in indicatorFeatures" :key="feature" class="flex items-start lg:col-span-1">
                  <div class="flex-shrink-0">
                    <Icon name="mdi:check" class="h-5 w-5 text-green-400" aria-hidden="true" />
                  </div>
                  <p class="ml-3 text-sm text-gray-700">{{ feature }}</p>
                </li>
              </ul>
            </div>
          </div>
          <div class="bg-gray-100 py-8 px-6 text-center lg:flex lg:flex-shrink-0 lg:flex-col lg:justify-center lg:p-12">
            <p class="text-lg font-medium leading-6 text-gray-900">Pay once, own it forever</p>
            <div class="mt-4 flex items-center justify-center text-5xl font-bold tracking-tight text-gray-900">
              <span>$25</span>
              <span class="ml-3 text-xl font-medium tracking-normal text-gray-500">GBP</span>
            </div>
            <div class="mt-6">
              <div class="rounded-md shadow">
                <a href="https://upgrade.chat/crypto-goats"
                  class="flex items-center justify-center rounded-md border border-transparent bg-gray-800 px-5 py-3 text-base font-medium text-white hover:bg-gray-900">Get
                  It</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>



  </div>
</template>
  
<script setup lang="ts">

var tabIndex = ref(0);
function changeIndex(newIndex: number) {
  tabIndex.value = newIndex;
  console.log(tabIndex)
}

const indicatorFeatures = [
  'Long Signals',
  'Short Signals',
  'Useful EMAs',
  'Symbol Stats on Chart',
]

const optionButtons = ["Monthly Billing", "Pay Once"];

const plans = [
  {
    title: 'FREE GOAT',
    featured: false,
    description: '',
    price: [0, 0],
    mainFeatures: [
      { id: 1, value: 'much more' },
    ],
  },
  {
    title: 'PREMIUM GOAT',
    featured: true,
    description: '',
    price: [40, 1250],
    mainFeatures: [
      { id: 1, value: 'Everything from Free' },
      { id: 2, value: 'much more' },
    ],
  },
  {
    title: 'ELITE GOAT',
    featured: false,
    description: '',
    price: [100, 2499.99],
    mainFeatures: [
      { id: 1, value: 'Everything from Premium' },
      { id: 2, value: 'much more' },
    ],
  },
]
</script>