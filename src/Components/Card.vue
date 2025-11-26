<script setup>
import IconsLike from './icons/like.vue';
import IconsPlus from './icons/plus.vue';
import IconsCheck from './icons/check.vue';

defineProps({
    tittle: String,
    imageUrl: String,
    price: Number,
    isFavorite: Boolean,
    isAdded: Boolean,
    onClickAdd: Function,
    onClickFavorite: Function
});
</script>

<template>
    <div>
        <div
            class="bg-white relative border border-gray-100 rounded-4xl p-8 cursor-pointer hover:-translate-y-2 duration-300 hover:shadow-xl">
            <IconsLike class="text-red-400 absolute top-8 left-8" v-if="isFavorite" @click="onClickFavorite" />
            <IconsLike class="text-gray-300 absolute top-8 left-8" v-else @click="onClickFavorite" />
            <img :src="imageUrl" alt="piccy">
            <p class="text-md mt-2">{{ tittle }}</p>

            <div class="flex justify-between mt-3">
                <div class="flex flex-col">
                    <span class="text-gray-500 text-sm">Цена: </span>
                    <b>{{ price }} ₽</b>
                </div>
                <div v-if="!isAdded">
                    <IconsPlus @click="onClickAdd" v-if="!isAdded" />
                </div>
                <div v-else>
                    <IconsCheck />
                </div>
            </div>
        </div>
    </div>
</template>