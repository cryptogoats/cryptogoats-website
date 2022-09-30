<template>
    <div class="relative overflow-hidden bg-blue-100">
        <div class="hidden sm:absolute sm:inset-y-0 sm:block sm:h-full sm:w-full" aria-hidden="true" data-aos="fade-top"
            data-aos-duration="1000">
            <div class="relative mx-auto h-full max-w-7xl">
                <svg class="absolute right-full translate-y-1/4 translate-x-1/4 transform lg:translate-x-1/2"
                    width="404" height="784" fill="none" viewBox="0 0 404 784">
                    <defs>
                        <pattern id="f210dbf6-a58d-4871-961e-36d5016a0f49" x="0" y="0" width="20" height="20"
                            patternUnits="userSpaceOnUse">
                            <rect x="0" y="0" width="4" height="4" class="text-blue-50" fill="currentColor" />
                        </pattern>
                    </defs>
                    <rect width="404" height="784" fill="url(#f210dbf6-a58d-4871-961e-36d5016a0f49)" />
                </svg>
                <svg class="absolute left-full -translate-y-3/4 -translate-x-1/4 transform md:-translate-y-1/2 lg:-translate-x-1/2"
                    width="404" height="784" fill="none" viewBox="0 0 404 784">
                    <defs>
                        <pattern id="5d0dd344-b041-4d26-bec4-8d33ea57ec9b" x="0" y="0" width="20" height="20"
                            patternUnits="userSpaceOnUse">
                            <rect x="0" y="0" width="4" height="4" class="text-blue-50" fill="currentColor" />
                        </pattern>
                    </defs>
                    <rect width="404" height="784" fill="url(#5d0dd344-b041-4d26-bec4-8d33ea57ec9b)" />
                </svg>
            </div>
        </div>

        <div class="relative pt-6 pb-16 sm:pb-24">
            <div class="mx-auto mt-16 max-w-7xl px-4 sm:mt-24 flex flex-col-reverse md:flex-row">
                <div class="lg:max-w-2/3 flex-shrink">
                    <p class="px-3 py-1 bg-blue-500 text-white rounded-full font-semibold w-fit text-xs mb-4"
                        data-aos="fade-right">THE TOP CRYPTO TRADING SERVER!</p>
                    <h1 class="text-6xl font-bold text-black" data-aos="fade-up">Join Crypto Goats Today!</h1>
                    <p class="py-6 text-3xl" data-aos="fade-up" data-aos-delay="100">Crypto Goats is the home of the
                        best Crypto
                        Traders, with numerous years of experience!
                        We provide Trading Signals, Low-Cap Crypto's, Risk Management and much more!</p>
                    <div class="space-x-4">
                        <a href="/pricing"
                            class="inline-block rounded-md border border-transparent bg-blue-500 py-2 px-4 text-base font-medium text-white hover:bg-opacity-75" data-aos="fade-right" >Join
                            Now!</a>
                        <a href="/pricing"
                            class="inline-block rounded-md border border-blue-500 bg-gray-50 py-2 px-4 text-base font-medium text-blue-600 hover:bg-blue-50" data-aos="fade-right" data-aos-delay="100">Pricing</a>
                    </div>
                    <h2 class="pt-16 text-blue-500" data-aos="fade-left">Partners & Supporters</h2>
                    <div class="flex">
                        <a v-for='partner, index in partners' :href='partner.link'><img :src="partner.image"
                                class="max-w-32 max-h-32 pr-4" data-aos="fade-up" :data-aos-delay='index*100+200' /></a>
                    </div>
                </div>
                <img src="https://pbs.twimg.com/profile_images/1518294991860293632/yeV2pyBa_400x400.jpg"
                    class="max-w-full w-md h-min rounded-lg shadow-2xl flex-1 object-contain hidden md:block" data-aos="flip-left" />
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">

interface Partner {
    link: string,
    image: string,
}

const partners: Partner[] = [
    {
        link: "https://promote.mexc.com/a/cryptogoats",
        image: "/img/mexc_saturation.png",
    },
    {
        link: "https://www.kucoin.com/r/af/QBSSSCCK",
        image: "/img/kucoin_saturation.png",
    },
    {
        link: "https://partner.bybit.com/b/cryptogoats",
        image: "/img/bybit_saturation.png",
    },
]


</script>

