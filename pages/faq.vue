<template>
  <div>
    <section class="text-gray-600 body-font bg-base-300">
      <div class="container px-5 py-24 mx-auto flex flex-wrap">
        <QAndA
          v-for="(question, index) in questions"
          :question="question.question"
          :answer="question.answer"
          :icon="question.icon"
          data-aos="fade-right"
          :data-aos-delay="index * 100"
        />
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
interface Question {
  question: string;
  answer: string;
  icon: string;
}

const questions: Question[] = [
  {
    question: "How do I pay?",
    answer:
      "We accept signups through Whop which has great integration with Discord! This makes it so the process of signing up is a lot easier! This also has a referral system meaning you can earn a share of the money when someone signs up using your link!",
    icon: "ic:baseline-question-mark",
  },
  {
    question: "When can I start?",
    answer:
      "Immediately! Sign up on the website and you can then make your purchase from Upgrade.Chat! This is a subscription based service where you can gain access monthly or yearly!",
    icon: "ic:baseline-question-mark",
  },
  {
    question: "Is There a Free Trial?",
    answer:
      "No, there isn't a free trial however we do have a free section in our Discord Server allowing you to learn the basics of Crypto without even having to spend a penny!",
    icon: "ic:baseline-question-mark",
  },
];
</script>
