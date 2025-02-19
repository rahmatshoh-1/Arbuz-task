<script setup>
import { ref } from "vue";

const listManager = ref([
    {
        id: 1,
        name: 'Дмитрий Иванов',
        position: 'Руководитель отдела маркетинга',
        imgUrl: './images/manager5.png',
        imgUrlIns: './images/instagram.png',
        imgUrlIn: './images/LinkedIn.png',
        linkIns: '#',
        linkIn: '#',
    },
    {
        id: 2,
        name: 'Ольга Соколова',
        position: 'Главный редактор',
        imgUrl: './images/manager6.png',
        imgUrlIns: './images/instagram.png',
        imgUrlIn: './images/LinkedIn.png',
        linkIns: '#',
        linkIn: '#',
    },
    {
        id: 3,
        name: 'Сергей Петров',
        position: 'Арт-директор',
        imgUrl: './images/manager7.png',
        imgUrlIns: './images/instagram.png',
        imgUrlIn: './images/LinkedIn.png',
        linkIns: '#',
        linkIn: '#',
    },
    {
        id: 4,
        name: 'Наталья Федорова',
        position: 'Маркетолог',
        imgUrl: './images/manager8.png',
        imgUrlIns: '',
        imgUrlIn: './images/LinkedIn.png',
        linkIns: '#',
        linkIn: '#',
    }
]);
</script>
<template>
    <div v-for="manager in listManager" :key="manager.id" class="rounded-2xl shadow-sm overflow-hidden">
        <div class="flex p-[20px] absolute z-10 gap-[10px]">
            <a class="hover:scale-110" href="#">
                <img class="" :src="manager.imgUrlIns" alt="">
            </a>
            <a class="hover:scale-110" href="#">
                <img class="" :src="manager.imgUrlIn" alt="">
            </a>
        </div>
        <img class="rounded-t-2xl cursor-pointer w-full ease-out duration-300 transition-all hover:scale-110"
            :src="manager.imgUrl" alt="">
        <div class="text-center relative py-[12px]  z-10 bg-white">
            <h3 class="text-lg font-semibold">{{ manager.name }}</h3>
            <p class="text-[#7D8CB4]">{{ manager.position }}</p>
        </div>
    </div>
</template>