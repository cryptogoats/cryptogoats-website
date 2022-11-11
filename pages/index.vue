<template>
  <div>
    <Hero />

    <!-- SERVICES -->
    <section class="text-gray-600 body-font">
      <div class="container px-5 py-24 mx-auto">
        <div class="flex flex-col text-center w-full mb-20">
          <h2 class="text-xs text-blue-600 tracking-widest font-medium mb-1">
            EXCLUSIVE FOR MEMEBERS
          </h2>
          <h1 class="sm:text-3xl text-2xl font-medium title-font text-gray-900">
            Access a variety of Services!
          </h1>
        </div>
        <div class="flex flex-wrap -m-4">
          <FeatureCard
            v-for="service in services"
            :title="service.title"
            :description="service.description"
            :items="service.items"
            :logo="service.logo"
            :icon="service.icon"
          />
        </div>
      </div>
    </section>

    <!-- STATISTICS -->
    <section class="bg-blue-600">
      <div class="container px-5 py-24 mx-auto">
        <div class="flex flex-col text-center w-full mb-20">
          <h1 class="sm:text-3xl text-2xl font-medium mb-4 text-white">
            Activate the Bullrun for your portfolio!
          </h1>
          <p class="lg:w-2/3 mx-auto leading-relaxed text-gray-100">
            Whether it is a Bullrun, or a Bear market, our skilled traders know
            how to trade level-to-level and increase your portfolio every single
            day. The crypto market moves fast, and with our trading formula, we
            ensure a highly profitable experience is delivered to you!
          </p>
        </div>
        <div class="flex flex-wrap -m-4 text-center">
          <StatisticsCard
            v-for="(statistic, index) in statistics"
            :title="statistic.title"
            :content="statistic.content"
            :icon="statistic.icon"
            data-aos="fade-up"
            :data-aos-delay="index * 100"
          />
        </div>
      </div>
    </section>

    <!-- REVIEWS -->
    <section class="text-gray-600 body-font">
      <div class="container px-5 py-24 mx-auto">
        <h1 class="text-3xl font-medium text-gray-900 mb-12 text-center">
          Testimonials
        </h1>
        <div class="flex flex-wrap -m-4">
          <TestimonialCard
            v-for="(testimonial, index) in testimonials"
            :reviewer="testimonial.reviewer"
            :content="testimonial.content"
            :source="testimonial.source"
            data-aos="fade-right"
            :data-aos-delay="index * 200"
          />
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
interface Service {
  title: string;
  description: string;
  items: String[] | undefined;
  logo: string;
  icon: string;
}

const services: Service[] = [
  {
    title: "Mentoring Lounge",
    description:
      "Our Newbie to Goat program will accelerate you through your crypto journey and boost you into becoming a GOAT trader!",
    items: [
      "Exclusive Crypto Courses!",
      "Long term cryptocurrency portfolios",
      "Risk Management Guides",
      "Confident Traders' Handbook",
    ],
    logo: "mdi:book-account-outline",
    icon: "mdi:comment-bookmark-outline",
  },
  {
    title: "Trading Centre",
    description:
      "We have 5 of the best crypto traders with over a 90% win rate, to give you the trading signals that will print you MONEY!",
    items: [
      "Short Term Scalps",
      "Long Term Holds",
      "Traders' Success",
      "Swing Trades",
    ],
    logo: "mdi:chart-line",
    icon: "mdi:currency-btc",
  },
  {
    title: "Goats Centre",
    description:
      "Interact with the Crypto Goats community members! The members are always welcome to chat about the crypto space and ongoing trades!",
    items: ["Low Cap Gems", "Chart Analysis", "Copy Trading", "NFTs"],
    logo: "mdi:castle",
    icon: "mdi:account-group-outline",
  },
];

interface Testimonial {
  content: string;
  reviewer: string;
  source: string;
}

const testimonials: Testimonial[] = [
  {
    content:
      "Just a quick review, I've been in this group since about January I think. I have never ever once thought 'I wonder if a different group would be better?' not a single time ever. I'm continually amazed by the amount of skill, maturity, composure, selflessness, accountability, friendship, commiseration etc in this group. This group honestly feels like a family. I've seen so much toxicity around the crypto community, and here, there is none I can't thank everyone enough for this opportunity.",
    reviewer: "Material_Sky",
    source: "Discord",
  },
  {
    content:
      "I have been in this server for about 2 weeks and I have nothing  but good things to say about it. The calls are great and all, but the admins are all very  active in the chats and will gladly answer any questions or provide charts upon requests. And thats really nice bc I have been in larger discords before and the admins hardly talk  with you, but in here they make the effort to make sure everyone is making money and learning. top notch discord group",
    reviewer: "thatsWild",
    source: "Discord",
  },
  {
    content:
      "I can't possibly completely explain my appreciation to the goats of this group/community. @Kazi | CG is truly the best, most accurate trader I've ever followed and @$S.C$| CG is by far the most knowledgeable trader I know of. They go above and beyond to ensure everyone's needs are completely accounted for and fulfilled. I'm so glad I came across this group and I have absolutely zero regrets about subscribing. My portfolio has only hit green for the time I've been here and yours will too! Happy trading everyone",
    reviewer: "BO55_JR",
    source: "Discord",
  },
  {
    content:
      "I consider myself a novice when it comes to trading crypto but I’m learning fast. One thing I learned today was that timing is everything! If you can jump on the calls made by the traders when they make them you can make big gains. I’m not riskingbig numbers as I’m still learning but I’m up 100% today because of the scalp calls and swing trades posted by @Kazi | CG and co. Thanks to all the traders and other members who offer help and advice.",
    reviewer: "Glewp",
    source: "Discord",
  },
];

interface Statistic {
  icon: string;
  content: string;
  title: string;
}

const statistics: Statistic[] = [
  {
    icon: "mdi:trophy-variant-outline",
    content: "91%",
    title: "Win Rate",
  },
  {
    icon: "mdi:account-group-outline",
    content: "1000+",
    title: "Members",
  },
  {
    icon: "ic:baseline-currency-exchange",
    content: "10+",
    title: "Expert Traders",
  },
  {
    icon: "mdi:heart-outline",
    content: "20K+",
    title: "Social Media Followers",
  },
];
</script>
