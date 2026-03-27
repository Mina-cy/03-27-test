<script setup>

</script>

<template>
    <div
        class="bg-blue-400 text-white w-[250px] h-[140px] flex items-center justify-between px-6 py-4 rounded-2xl shadow-lg border border-blue-300">
        <div class="text-3xl">
            <i class="fa-solid fa-user"></i>
        </div>

        <div class="flex flex-col items-start gap-1 min-w-0 flex-1 ml-4">
            <span class="text-sm font-medium">
                <slot name="title">今日累積</slot>
            </span>
            <span class="text-lg font-bold">
                <slot name="sub"></slot>
            </span>
        </div>

        <div class="text-3xl font-black">
            <slot name="value">10</slot>
        </div>
    </div>
</template>


<style scoped></style>