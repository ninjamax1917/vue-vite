<script setup>
import Header from './Components/Header.vue';
import CardList from './Components/CardList.vue';
import Drawer from './Components/Drawer.vue';
import Search from './Components/icons/search.vue';

</script>

<template>
    <!-- <Drawer /> -->
    <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-14">
        <Header />

        <div class="p-10">
            <div class="flex justify-between items-center">
                <h2 class="text-3xl font-bold mb-8">Пиццы</h2>
                <div class="flex gap-4">
                    <select class="py-2 px-3 border border-gray-100 rounded-2xl outline-none">
                        <option>
                            По названию
                        </option>
                        <option>
                            По цене (дешевле)
                        </option>
                        <option>
                            По цене (дороже)
                        </option>
                    </select>

                    <div class="relative">
                        <Search class="absolute left-3 top-1.5 text-gray-300" />
                        <input
                            class="border border-gray-200 rounded-md py-1.5 pl-12 pr-4 outline-none focus:border-gray-400"
                            placeholder="Поиск..." type="text">
                    </div>
                </div>
            </div>
        </div>

        <CardList />

    </div>
</template>

<style scoped></style>