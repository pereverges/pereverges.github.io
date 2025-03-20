<script setup></script>

<template>
    <!-- Hero Section Start -->
    <div class="container mx-auto px-5 overflow-x-hidden lg:overflow-x-visible">
        <section class="grid grid-cols-none lg:grid-cols-2 pb-16 pt-8 items-center">
            <div class="lg:w-5/6 order-1 lg:order-none ml-auto overflow-hidden rounded-lg">
                <img class="z-10 w-full max-h-[60vh] object-contain rounded-[20px]" src="/images/CheckInAlert.jpeg" />
            </div>

            <div class="lg:w-5/6 order-1 lg:order-none">
                <h1 class="text-4xl xl:text-5xl font-bold font-theme-heading text-center">The App</h1>
                <h1 class="text-4xl xl:text-5xl font-bold font-theme-heading text-center">For Anyone Who</h1>
                <h1 class="text-4xl xl:text-5xl font-bold font-theme-heading text-center">Lives Alone</h1>

                <p class="lg:text-3xl mt-10 font-theme-content text-theme-grayish-blue text-center">Alerts Family & Friends</p>
                <p class="lg:text-3xl font-theme-content text-theme-grayish-blue text-center">If Your Phone Doesn't Move</p>
                <div class="flex justify-center mt-10">
                    <LinkButton btn-type="primary" link="#download-section">iOS</LinkButton>
                    <LinkButton btn-type="muted" link="#download-section">Android</LinkButton>
                </div>
            </div>


        </section>
        <p class="lg:text-3xl font-bold font-theme-heading text-center">No Actions Nedded! No Buttons To Push!</p>
        <p class="lg:text-3xl font-theme-content text-theme-grayish-blue text-center">If your phone doesn't move in a time you set,</p>
        <p class="lg:text-3xl font-theme-content text-theme-grayish-blue text-center">your friends and family will get a text so they</p>
        <p class="lg:text-3xl font-theme-content text-theme-grayish-blue text-center">can check on you.</p>

    </div>
    <!-- Hero Section End -->
</template>
