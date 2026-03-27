<script setup>
import { computed } from "vue"
import Nav from '@/components/Nav.vue';
import Card from '@/components/Card.vue';
import BigCard from '@/components/BigCard.vue';
const cards = computed(() => [
    { title: "今日人容數", sub: "", value: "10" },
    { title: "今日累積", sub: "未帶安全帽次數", value: "10" },
    { title: "今日累積", sub: "危險區域警報次數", value: "10" },
    { title: "本週累積", sub: "未帶安全帽次數", value: "10" },
    { title: "本週累積", sub: "危險區域警報次數", value: "0" },
])
</script>

<template>
    <div class="flex w-[300px] h-screen">
        <Nav />
        <div class="flex-1 p-15">
            <div class="flex justify-center lg:gap-5 mb-6">
                <Card v-for="(card) in cards">
                    <template #title>{{ card.title }}</template>
                    <template #sub>{{ card.sub }}</template>
                    <template #value>{{ card.value }}</template>
                </Card>
            </div>
            <div class="flex justify-center gap-6">
                <BigCard />
                <BigCard />
            </div>
        </div>
    </div>
</template>

<style scoped></style>