<template>
    <div class="container bg-[#1e2242] p-6">
        <div class="mb-6">
            <h1 class="text-white">THIS FOR LOGO</h1>
        </div>
        <hr class="h-[2px] w-full bg-[#cdff63]">
        <div class="flex flex-row mt-5">
            <div class="w-1/2 text-white">
                <h3>ABOUT</h3>
                <ul class="mt-3" v-for="(list, id) in footerListAbout" :key="id">
                    <li class="text-sm leading-8 cursor-pointer hover:underline">
                        {{ list }}
                    </li>

                </ul>
            </div>

            <div class="w-1/2 text-white">
                <h3>INFORMATION</h3>
                <ul class="mt-3" v-for="(list, id) in footerListInformation" :key="id">
                    <li class="text-sm leading-8 cursor-pointer hover:underline">
                        {{ list }}
                    </li>
                </ul>
            </div>


        </div>

        <div class="flex flex-col mt-5">
            <h3 class="text-white">SUBSCRIBE TO OUR NEWSLETTER</h3>
            <div class="flex flex-row mt-3 mb-4">
                <div class="w-1/2">
                    <label for="search" class="mb-2 text-sm font-medium text-gray-900 sr-only dark:text-white">Email</label>
                    <div class="relative">
                        <div class="absolute inset-y-0 start-0 flex items-center ps-3 pointer-events-none">
                            <svg class="w-4 h-4 text-gray-500 dark:text-gray-400" aria-hidden="true"
                                xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 20 16">
                                <path
                                    d="m10.036 8.278 9.258-7.79A1.979 1.979 0 0 0 18 0H2A1.987 1.987 0 0 0 .641.541l9.395 7.737Z" />
                                <path
                                    d="M11.241 9.817c-.36.275-.801.425-1.255.427-.428 0-.845-.138-1.187-.395L0 2.6V14a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V2.5l-8.759 7.317Z" />
                            </svg>
                        </div>
                        <input type="search" id="search"
                            class="block w-full p-4 ps-10 text-sm text-gray-900 border border-gray-300 rounded-lg bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                            placeholder="Email" required>
                        <button type="submit"
                            class="text-white absolute end-2.5 bottom-2.5 bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-4 py-2 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">Subscribe</button>
                    </div>
                </div>
                <div class="w-1/2">
                    <ul class="flex flex-row justify-end gap-4">
                        <li class="text-[#fe3ca7] border-2 border-[#fe3ca7] px-3 py-2 rounded-full text-2xl">
                            <i class="mdi mdi-instagram"></i>
                        </li>
                        <li class="text-[#fe3ca7] border-2 border-[#fe3ca7] px-3 py-2 rounded-full text-2xl">
                            <i class="mdi mdi-facebook"></i>
                        </li>
                        <li class="text-[#fe3ca7] border-2 border-[#fe3ca7] px-3 py-2 rounded-full text-2xl">
                            <i class="mdi mdi-pinterest"></i>
                        </li>
                    </ul>
                </div>
            </div>
            <hr class="h-[2px] w-full bg-[#cdff63]">
            <div class="flex flex-row justify-end mt-2">
                <p class="text-white">© 2024, Not Another Bill</p>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const footerListAbout = ref(['Our Story', 'Personalisation', 'Corporate Gift', 'Rewards Club', 'Affiliates'])
const footerListInformation = ref(['FAQs', 'Delivery & Returns', 'Jobs', 'Terms & Conditions / Privacy', 'Contact'])
</script>