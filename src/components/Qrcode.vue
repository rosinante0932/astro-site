<template>
    <div class="relative" :class="className">
        <img src="/assets/yhicon.png" alt="下载链接二维码" class="w-[40px] absolute left-[50%] top-[50%] translate-[-50%]">
        <QrcodeVue :value="text" :size="size" level="Q" />
    </div>
</template>

<script setup lang="ts">
import QrcodeVue from 'qrcode.vue'
import { ref } from 'vue'
defineProps(['size', 'url', 'className'])
const text = ref(`https://example.com?rd=${Math.random()}`) // 扫码内容


</script>
