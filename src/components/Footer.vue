<script setup>
import { ref } from 'vue'
const activeMenu = ref('about');

const changeMenu = (item) => {
    activeMenu.value = item
}
</script>
<template>
    <footer class="p-[24px] md:pt-[70px] md:pb-[45px] bg-[#F1F4FD] text-[#0048CE]">
        <div class="flex flex-col md:flex-row container mx-auto">
            <div class="md:w-4/12">
                <img src="../../public/images/logo.svg" alt="">
                <ul class="mt-[18px] md:mt-[116px]">
                    <li>
                        <a class="hover:text-[#799EE5]" href="#">
                            Москва, БЦ «Лотос», ул. Ленинская, 19
                        </a>
                    </li>
                    <li>
                        <a class="hover:text-[#799EE5]" href="#">
                            +7 999 854 85 85 — Москва
                        </a>
                    </li>
                    <li>
                        <a class="hover:text-[#799EE5]" href="#">
                            +7 914 487 38 38 — Владивосток
                        </a>
                    </li>
                    <li>
                        <a class="hover:text-[#799EE5]" href="#">
                            hello@estate.ru
                        </a>
                    </li>
                </ul>
                <div class="flex mt-[20px] md:mt-[16px]">
                    <a href="#">
                        <img src="../../public/images/telegram.png" alt="">
                    </a>
                    <a href="#">
                        <img src="../../public/images/whatsapp.png" alt="">
                    </a>
                </div>
            </div>
            <div class="md:w-8/12">
                <div class="flex flex-col md:flex-row my-[20px]">
                    <div class="border-b py-2">
                        <span @click="changeMenu('about')"
                            class="flex pb-2 items-center justify-between text-[#799EE5]">О компании
                            <svg class="md:hidden" :class="{ 'rotate-180': activeMenu !== 'about' }" width="10" height="6"
                                viewBox="0 0 10 6" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9.48483 5.24271L5.24219 1.00007L0.999547 5.24271" stroke="#0048CE" />
                            </svg>
                        </span>
                        <ul :class="[`md:mr-[90px] md:block`, { 'hidden': activeMenu !== 'about' }]">
                            <li class="my-[4px]">
                                <a class="hover:text-[#799EE5]" href="#">О нас</a>
                            </li>
                            <li class="mb-[4px]">
                                <a class="hover:text-[#799EE5]" href="#">Команда</a>
                            </li>
                            <li class="mb-[4px]">
                                <a class="hover:text-[#799EE5]" href="#">Контакты</a>
                            </li>
                            <li  class="mb-[4px]">
                                <a class="hover:text-[#799EE5]" href="#">Блог</a>
                            </li>
                        </ul>
                    </div>
                    <div class="border-b py-2">
                        <span @click="changeMenu('realEstate')"
                            class="flex pb-2 items-center justify-between text-[#799EE5]">Недвижимость
                            <svg class="md:hidden" :class="{ 'rotate-180': activeMenu !== 'realEstate' }" width="10" height="6"
                                viewBox="0 0 10 6" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9.48483 5.24271L5.24219 1.00007L0.999547 5.24271" stroke="#0048CE" />
                            </svg>
                        </span>
                        <ul :class="[`md:mr-[90px] md:block`, { 'hidden': activeMenu !== 'realEstate' }]">

                            <li class="my-[4px]">
                                <a class="hover:text-[#799EE5]" href="#">Жилая</a>
                            </li>
                            <li class="mb-[4px]">
                                <a class="hover:text-[#799EE5]" href="#">Коммерческая</a>
                            </li>
                            <li class="mb-[4px]">
                                <a class="hover:text-[#799EE5]" href="#">Инвестиционная</a>
                            </li>
                        </ul>
                    </div>
                    <div class="border-b py-2">
                        <span @click="changeMenu('service')"
                            class="flex items-center justify-between text-[#799EE5]">Услуги
                            <svg class="md:hidden" :class="{ 'rotate-180': activeMenu !== 'service' }" width="10" height="6"
                                viewBox="0 0 10 6" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9.48483 5.24271L5.24219 1.00007L0.999547 5.24271" stroke="#0048CE" />
                            </svg>
                        </span>
                        <ul :class="[`md:mr-[90px] md:block`, { 'hidden': activeMenu !== 'service' }]">

                            <li class="my-[4px]">
                                <a class="hover:text-[#799EE5]" href="#">По подбору недвижимости</a>
                            </li>
                            <li class="mb-[4px]">
                                <a class="hover:text-[#799EE5]" href="#">Юридическое сопровождение</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <p class="mt-[80px]">© 2025 Estate. Все права защищены. При копировании материалов сайта ссылка на
                    источник обязательна.
                    Политика конфиденциальности • Соглашение об использовании</p>
            </div>
        </div>
    </footer>
</template>
