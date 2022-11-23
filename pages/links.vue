<template>
  <div
    class="flex flex-col items-center justify-center min-h-screen min-w-screen bg-black overflow-hidden pb-32"
  >
    <div
      class="h-16 md:h-24 lg:h-32 my-4"
      data-aos="fade-down"
      data-aos-delay="300"
    >
      <img
        src="https://pbs.twimg.com/profile_images/1594547861169082370/p0mtt_-6_400x400.jpg"
        class="h-16 md:h-24 lg:h-32"
      />
    </div>
    <Link
      v-for="(link, index) in links"
      :url="link.url"
      :name="link.name"
      :icon="link.icon"
      :delay="index * 100"
    />
    <div class="h-1 w-32 bg-gray-700 my-3"></div>
    <Link
      v-for="(link, index) in partners"
      :url="link.url"
      :name="link.name"
      :icon="link.icon"
      :delay="index * 100"
    />
  </div>
</template>

<style>
html,
body {
  margin: 0;
  padding: 0;
}
</style>

<script setup lang="ts">
definePageMeta({
  layout: "link",
});
const links = [
  {
    url: "https://cryptogoats.net",
    icon: "mdi:web",
    name: "Website",
  },
  {
    url: "https://discord.gg/hnQH7vhFwS",
    icon: "mdi:discord",
    name: "Discord",
  },
  {
    url: "https://twitter.com/cryptogoatss",
    icon: "mdi:twitter",
    name: "Twitter",
  },
];
const partners = [
  {
    url: "https://promote.mexc.com/a/cryptogoats",
    icon: "mdi:bank-transfer",
    name: "MEXC",
  },
  {
    url: "https://partner.bybit.com/b/cryptogoats",
    icon: "mdi:bank-transfer",
    name: "ByBit",
  },
  {
    url: "https://www.kucoin.com/r/af/QBSSSCCK",
    icon: "mdi:bank-transfer",
    name: "KuCoin",
  },
];
</script>
