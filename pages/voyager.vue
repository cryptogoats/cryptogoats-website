<template>
  <div>
    <iframe :src="url" class="min-w-full min-h-screen" scrolling="no" />
  </div>
</template>

<script setup>
const baseUrl = "https://app.thevoyager.io/swap";

const configuration = {
  isWidget: true,
  widgetId: "56",
  logoURI: "https://cryptogoats.net/favicon.ico",
};

const paramString = new URLSearchParams(configuration).toString();
const url = `${baseUrl}?${paramString}`;
</script>
