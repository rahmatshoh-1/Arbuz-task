<script setup>
import { ref } from "vue";

const listInvest = ref([
    {
        id: 1,
        name: 'Анна Васильева',
        position: 'Операционный директор',
        imgUrl: './images/manager1.png',
        imgUrlIns: './images/instagram.png',
        imgUrlIn: './images/LinkedIn.png',
        linkIns: '#',
        linkIn: '#',
    },
    {
        id: 2,
        name: 'Елена Морозова',
        position: 'Инвестиционный консультант',
        imgUrl: './images/manager2.png',
        imgUrlIns: './images/instagram.png',
        imgUrlIn: './images/LinkedIn.png',
        linkIns: '#',
        linkIn: '#',
    },
    {
        id: 3,
        name: 'Мария Кузнецова',
        position: 'Инвестиционный консультант',
        imgUrl: './images/manager3.png',
        imgUrlIns: './images/instagram.png',
        imgUrlIn: './images/LinkedIn.png',
        linkIns: '#',
        linkIn: '#',
    },
    {
        id: 4,
        name: 'Алексей Смирнов',
        position: 'Инвестиционный консультант',
        imgUrl: './images/manager4.png',
        imgUrlIns: '',
        imgUrlIn: './images/LinkedIn.png',
        linkIns: '#',
        linkIn: '#',
    }
]);
</script>
<template>
    <div v-for="invest in listInvest" :key="invest.id"
        class="rounded-2xl shadow-sm overflow-hidden">
        <div class="flex p-[20px] absolute z-10 gap-[10px]">
            <a class="hover:scale-110" href="#">
                <img class="" :src="invest.imgUrlIns" alt="">
            </a>
            <a class="hover:scale-110" href="#">
                <img class="" :src="invest.imgUrlIn" alt="">
            </a>
        </div>
        <img class="rounded-t-2xl cursor-pointer w-full ease-out duration-300 transition-all hover:scale-110"
            :src="invest.imgUrl" alt="">
        <div class="text-center relative py-[12px]  z-10 bg-white">
            <h3 class="text-lg font-semibold">{{ invest.name }}</h3>
            <p class="text-[#7D8CB4]">{{ invest.position }}</p>
        </div>
    </div>
</template>