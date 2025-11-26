<script setup>
import CloseIcon from './icons/close.vue';
</script>

<template>
    <div class="flex items-center border border-slate-100 p-4 rounded-xl gap-4">
        <img class="w-20 h-20" src="/images/products/piccy/hunting.png" alt="piccy">

        <div class="flex flex-col">
            <p class="text-sm">
                Пицца Lorem ipsum dolor sit amet.
            </p>

            <div class="flex justify-between mt-1">
                <b class="text-sm">12990 ₽</b>
                <CloseIcon class="opacity-40 hover:opacity-100 cursor-pointer transition w-5 h-5" />
            </div>
        </div>
    </div>
</template>



<style scoped></style>