<script setup>
import { ref } from "vue";
const showMenu = ref(false)
</script>
<template>
    <header class="py-[25px]">
        <div class="hidden lg:flex flex-col lg:flex-row  justify-between items-center container mx-auto text-[#0048CE]">
            <a href="#">
                <img src="../../public/images/logo.svg" alt="">
            </a>
            <ul class="hidden md:flex justify-between items-center gap-[52px]">
                <li class="flex flex-col items-center relative group">
                    <span
                        class="hover:text-blue-600 transition cursor-pointer hover:bg-blue-100 py-2 flex items-center gap-3">Недвижимость
                        <svg width="7" height="5" viewBox="0 0 7 5" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M6.5 0.5L3.50163 3.5L0.503263 0.5" stroke="#0048CE" />
                        </svg>
                    </span>
                    <ul
                        class="ml-4 cursor-pointer transition bg-blue-50 py-2 px-4 rounded-2xl absolute z-10 hidden group-hover:block">
                        <li class="border-b-2 pb-2 flex gap-4 items-center">Недвижимость
                            <svg class="rotate-180" width="7" height="5" viewBox="0 0 7 5" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M6.5 0.5L3.50163 3.5L0.503263 0.5" stroke="#0048CE" />
                            </svg>

                        </li>
                        <li class="my-1">Жилая</li>
                        <li class="mb-1">Коммерческая</li>
                        <li class="mb-1">Инвестиционная</li>
                        <li class="mb-1">Эксклюзивная</li>
                    </ul>
                </li>

                <li class="hover:bg-blue-50 px-[20px] py-2 rounded-2xl"><a href="#">Услуги</a></li>
                <li class="hover:bg-blue-50 px-[20px] py-2 rounded-2xl"><a href="#">Блог</a></li>
                <li class="hover:bg-blue-50 px-[20px] py-2 rounded-2xl"><a href="#">О компании</a></li>
            </ul>
            <ul class="hidden lg:flex  items-center gap-[20px]">
                <li class="flex">
                    <a href="#">
                        <img src="../../public/images/telegram.png" alt="">
                    </a>
                    <a href="#">
                        <img src="../../public/images/whatsapp.png" alt="">
                    </a>
                </li>
                <li><a href="tel:+79998548585">+7 999 854 85 85</a></li>
                <li class="underline"><a href="#">En</a></li>
            </ul>
        </div>
        <!-- mobile -->
        <div
            class="lg:hidden px-[24px] py-2 rounded-2xl flex flex-col lg:flex-row  justify-between container mx-auto text-[#0048CE]">
            <div class="flex justify-between items-center py-[20px]">
                <a href="#">
                    <img src="../../public/images/logo.svg" alt="">
                </a>
                <div class="flex justify-between items-center gap-[40px]">
                    <a href="#">En</a>
                    <button @click="showMenu = !showMenu" type="button">
                        <img v-if="!showMenu"  src="../../public/images/Burger.png" alt="">
                        <img v-if="showMenu" src="../../public/images/close.png" alt="">
                    </button>
                </div>
            </div>
            <ul v-if="showMenu" class="flex flex-col justify-between">
                <li class="flex-start flex-col">
                    <span class="text-[30px]">Недвижимость</span>
                    <ul class="ml-2">
                        <li>Жилая</li>
                        <li>Коммерческая</li>
                        <li>Инвестиционная</li>
                        <li>Эксклюзивная</li>
                    </ul>
                </li>
                <li class="text-[30px]"><a href="#">Услуги</a></li>
                <li class="text-[30px]"><a href="#">Блог</a></li>
                <li class="text-[30px]"><a href="#">О компании</a></li>
            </ul>
            <ul v-if="showMenu" class="flex flex-col mt-[60px] mb-[10px]">
                <li><a href="tel:+79998548585">+7 999 854 85 85 — Москва</a></li>
                <li><a href="tel:+79144873838">+7 914 487 38 38 — Владивосток</a></li>
                <li class="flex">
                    <a href="#">
                        <img src="../../public/images/telegram.png" alt="">
                    </a>
                    <a href="#">
                        <img src="../../public/images/whatsapp.png" alt="">
                    </a>
                </li>
            </ul>
        </div>
    </header>
</template>