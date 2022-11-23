<template>
  <footer class="bg-amber-600 z-50" aria-labelledby="footer-heading">
    <h2 id="footer-heading" class="sr-only">Footer</h2>
    <div class="mx-auto max-w-7xl py-12 px-4 sm:px-6 lg:py-16 lg:px-8">
      <div class="xl:grid xl:grid-cols-3 xl:gap-8">
        <div class="grid grid-cols-2 gap-8 xl:col-span-2">
          <div>
            <h3 class="text-base font-medium text-amber-100">PARTNERS</h3>
            <ul role="list" class="mt-4 space-y-4">
              <li v-for="item in navigation.partners" :key="item.name">
                <a
                  :href="item.href"
                  class="text-base text-amber-400 hover:text-amber-300"
                  >{{ item.name }}</a
                >
              </li>
            </ul>
          </div>
          <div>
            <h3 class="text-base font-medium text-amber-100">INFO</h3>
            <ul role="list" class="mt-4 space-y-4">
              <li v-for="item in navigation.info" :key="item.name">
                <a
                  :href="item.href"
                  class="text-base text-amber-400 hover:text-amber-300"
                  >{{ item.name }}</a
                >
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div
        class="mt-8 border-t border-amber-100 pt-8 md:flex md:items-center md:justify-between"
      >
        <div class="flex space-x-6 md:order-2">
          <a
            v-for="item in navigation.social"
            :key="item.name"
            :href="item.href"
            class="text-white hover:text-amber-100"
          >
            <span class="sr-only">{{ item.name }}</span>
            <Icon
              :name="item.icon"
              class="h-6 w-6 text-xl text-white"
              aria-hidden="true"
            />
          </a>
        </div>
        <p class="mt-8 text-base text-white md:order-1 md:mt-0">
          &copy; CryptoGoats
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
const navigation = {
  info: [{ name: "Frequently asked Questions", href: "/faq" }],
  partners: [
    { name: "MEXC", href: "https://promote.mexc.com/a/cryptogoats" },
    { name: "KuCoin", href: "https://www.kucoin.com/r/af/QBSSSCCK" },
    { name: "ByBit", href: "https://partner.bybit.com/b/cryptogoats" },
    { name: "VaultFinance", href: "/vaultfinance" },
    { name: "Voyager", href: "/voyager" },
  ],
  social: [
    {
      name: "Twitter",
      href: "https://twitter.com/CryptoGoatss",
      icon: "mdi:twitter",
    },
    {
      name: "GitHub",
      href: "https://github.com/cryptogoats",
      icon: "mdi:github",
    },
  ],
};
</script>
