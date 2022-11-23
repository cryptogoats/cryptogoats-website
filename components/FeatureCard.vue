<template>
  <div class="p-4 md:w-1/3">
    <div
      class="flex rounded-lg h-full bg-gray-100 p-8 flex-col shadow-xl"
      data-aos="fade-up"
    >
      <div class="flex items-center mb-3" data-aos="fade-up">
        <div
          class="w-8 h-8 mr-3 inline-flex items-center justify-center rounded-full flex-shrink-0"
        >
          <Icon :name="logo" size="1.5em" class="text-amber-600" />
        </div>
        <h2 class="text-black text-lg title-font font-medium">{{ title }}</h2>
      </div>
      <div class="flex-grow">
        <p
          class="leading-relaxed text-gray-800 pb-4 text-justify"
          data-aos="fade-up"
          data-aos-delay="100"
        >
          {{ description }}
        </p>
        <div
          class="flex flex-col sm:items-start sm:text-left text-center items-center -mb-1 space-y-2.5"
        >
          <p v-for="item in items" data-aos="fade-up" data-aos-delay="200">
            <span
              class="bg-white text-amber-600 w-6 h-6 mr-2 rounded-full inline-flex items-center justify-center"
            >
              <Icon :name="icon" class="w-4" />
            </span>
            <span class="text-gray-800">
              {{ item }}
            </span>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps({
  title: String,
  description: String,
  items: Array<String>,
  logo: String,
  icon: String,
});
</script>
