<script setup>
import ProductCard from './Card.vue';

const onClickAdd = () => alert('Добавлено в корзину!');
</script>

<template>
    <div class="grid grid-cols-4 gap-5">
        <ProductCard tittle="Пицца охотничья" imageUrl="/images/products/piccy/hunting.png" :price="450"
            :isAdded="false" :onClickAdd="onClickAdd" />
    </div>
</template>



<style scoped></style>