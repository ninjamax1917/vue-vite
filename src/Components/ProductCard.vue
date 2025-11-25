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
});

const onClickAdd = () => {
    alert(1);
}
</script>

<template>
    <div>
        <div
            class="bg-white relative border border-gray-100 rounded-4xl p-8 cursor-pointer hover:-translate-y-2 duration-300 hover:shadow-xl">
            <IconsLike class="text-red-400 absolute top-8 left-8" v-if="isFavorite" />
            <IconsLike class="text-gray-300 absolute top-8 left-8" v-else />
            <img :src="imageUrl" alt="piccy">
            <p class="text-md mt-2">{{ tittle }}</p>

            <div class="flex justify-between mt-3">
                <div class="flex flex-col">
                    <span class="text-gray-500 text-sm">Цена: </span>
                    <b>{{ price }} ₽</b>
                </div>
                <div>
                    <IconsPlus @click="onClickAdd" v-if="!isAdded" />
                    <IconsCheck v-else />
                </div>
            </div>

        </div>
    </div>
</template>