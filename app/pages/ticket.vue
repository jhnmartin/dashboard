<script lang="ts" setup>
import { useQRCode } from "@vueuse/integrations/useQRCode";
import { ref } from "vue";

const text = ref("https//www.barcrawllive.com");
const qrcode = useQRCode(text);
</script>

<template>
  <input v-model="text" type="text" />
  <img :src="qrcode" alt="QR Code" class="w-48 h-48 dark:invert" />
</template>
