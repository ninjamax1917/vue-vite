<script setup>
// Импортируем иконки
import IconsShoppingCart from './icons/shopping-cart.vue';
import IconsHeart from './icons/heart.vue';
import IconsProfile from './icons/profile.vue';
</script>

<template>


    <header class="flex justify-between border-b border-slate-100 px-10">
        <a href="/">
            <div class="flex items-center gap-x-0">
                <div class="flex flex-col items-center">
                    <span class="span_tittle">kapi</span>
                    <span class="span_subtittle">Горячая пицца</span>
                </div>
                <!-- КАРТИНКА-ЛОГО -->
                <img class="w-20 h-20 -mx-1 mt-2" src="/images/logo/kapi.png" alt="Logo">
                <!--  -->
                <div class="flex flex-col items-center">
                    <span class="span_tittle">pi<span class="zz span_tittle">zz</span class="span_tittle">a</span>
                    <span class="span_subtittle">быстрая доставка</span>
                </div>
            </div>
        </a>
        <ul class="flex items-center gap-10">
            <li class="flex items-center gap-3 text-gray-500 hover:text-[#D55126] cursor-pointer duration-300">
                <IconsShoppingCart />
                <span>1205 руб.</span>
            </li>
            <li class="flex items-center gap-3 text-gray-500 hover:text-[#D55126] cursor-pointer duration-300">
                <IconsHeart />
                <span>Закладки</span>
            </li>
            <li class="flex items-center gap-3 text-gray-500 hover:text-[#D55126] cursor-pointer duration-300">
                <IconsProfile />
                <span>Профиль</span>
            </li>

        </ul>
    </header>
</template>

<style scoped>
.span_tittle {
    font-size: 44px;
    font-weight: bold;
    text-transform: uppercase;
}

.span_subtittle {
    font-size: 12px;
    font-weight: normal;
    margin-top: -8px;
    text-transform: uppercase;
    color: #364153;
    /* #364153 */
}

.zz {
    color: #D55126;
}
</style>
