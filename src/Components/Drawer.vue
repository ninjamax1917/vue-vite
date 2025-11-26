<script setup>
import Arrow from './icons/arrow.vue';
import CartItemList from './CartItemList.vue';
</script>

<template>
    <div class="fixed top-0 left-0 h-full w-full bg-black z-10 opacity-60"></div>
    <div class="bg-white w-96 h-full fixed right-0 top-0 z-20 p-8">
        <div class="flex items-center gap-5 mb-8">
            <button class="opacity-30 cursor-pointer hover:opacity-100 transition hover:translate-x-1">
                <Arrow />
            </button>
            <h2 class="text-2xl font-bold">Корзина</h2>
        </div>
        <CartItemList />

        <div class="flex flex-col gap-4 my-7">
            <div>
                <div class="flex gap-2">
                    <span>Итого:</span>
                    <div class="flex-1 border-b border-dashed"></div>
                    <b>12900 ₽</b>
                </div>
            </div>

            <div>
                <div class="flex gap-2">
                    <span>Налог 5%:</span>
                    <div class="flex-1 border-b border-dashed"></div>
                    <b>900 ₽</b>
                </div>
            </div>
            <button disabled="true"
                class="mt-4 bg-lime-500 hover:bg-lime-600 active:bg-lime-700 disabled:bg-slate-300 disabled:cursor-default cursor-pointer transition w-full rounded-2xl py-3 mb-5 text-lg font-semibold text-white">
                Оформить заказ
            </button>
        </div>
    </div>
</template>