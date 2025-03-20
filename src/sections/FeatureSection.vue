<script setup>

import features from '../data/features.js';
import { ref } from 'vue';

let isOpen = ref(1);

</script>

<template>
    <!-- Features Section Start -->
    <div id="features" class="container mx-auto px-5">
        <section class="py-16">
            <div class="w-4/5 md:w-3/5 mx-auto">
                <h1 class="text-4xl xl:text-5xl font-bold font-theme-heading text-center">How it works!</h1>
                <!--p class="text-theme-grayish-blue text-center mt-7 font-theme-content text-lg">Our aim is to make it quick and easy for you to access your favourite websites. Your bookmarks sync between your devices so you can access them on the go.</p-->
            </div>

            <section class="grid grid-cols-none lg:grid-cols-4 pb-16 pt-8 items-center">
                <div class="lg:w-5/6 order-1 lg:order-none">
                    <h1 class="text-2xl xl:text-2xl font-bold font-theme-heading text-center">1. Sign up</h1>
                    <img class="z-10 w-full" src="/images/CheckInAlert.jpeg" />
                </div>

                <div class="lg:w-5/6 order-1 lg:order-none">
                    <h1 class="text-2xl xl:text-2xl font-bold font-theme-heading text-center">2. Add Contacts</h1>
                    <img class="z-10 w-full" src="/images/CheckInAlert.jpeg" />
                </div>

                <div class="lg:w-5/6 order-1 lg:order-none">
                    <h1 class="text-2xl xl:text-2xl font-bold font-theme-heading text-center">3. Set the Timer</h1>
                    <img class="z-10 w-full" src="/images/CheckInAlert.jpeg" />
                </div>

                <div class="lg:w-5/6 order-1 lg:order-none">
                    <h1 class="text-2xl xl:text-2xl font-bold font-theme-heading text-center">4. Relax</h1>
                    <img class="z-10 w-full" src="/images/CheckInAlert.jpeg" />
                </div>


            </section>

            <div class="mt-10">
                <ul class="flex flex-col items-center md:flex-row justify-center font-theme-heading">
                    <li v-for="feature in features" :key="feature.id" :class="isOpen === feature.id ? 'md:border-b-4 md:border-theme-secondary' : ''" class="w-full md:w-56 cursor-pointer hover:text-theme-secondary transition duration-200 border-b-2 border-t-2 md:border-t-0 flex justify-center">
                        <a @click.prevent="isOpen = feature.id" href="#" :class="isOpen === feature.id ? ' border-theme-secondary' : ''" class="py-5  md:border-b-0 border-b-4">{{ feature.name }}</a>
                    </li>
                </ul>
            </div>

            <div class="mt-16">
                <!-- Tab Content -->
                <template v-for="feature in features" :key="feature.id">
                    <div v-show="isOpen === feature.id" class="grid gap-32 lg:grid-cols-2 items-center">
                        <div class="relative">
                            <img class="z-10 w-full" :src="feature.details.imageUrl" />
                            <div class="-z-10 bg-theme-primary h-52 w-96 sm:h-80 sm:w-full rounded-r-full absolute -left-56 -bottom-16"></div>
                        </div>
                        <div>
                            <h3 class="font-theme-heading text-2xl md:text-3xl font-medium text-center lg:text-left">{{ feature.details.title }}</h3>
                            <p class="mt-7 font-theme-content text-lg text-theme-grayish-blue text-center lg:text-left">{{ feature.details.description }}</p>
                            <div class="flex justify-center lg:justify-start mt-7">
                                <LinkButton btn-type="primary" :link="feature.details.link">More Info</LinkButton>
                            </div>
                        </div>
                    </div>
                </template>
                <!-- Tab Content -->
            </div>
        </section>
    </div>
    <!-- Features Section End -->
</template>
