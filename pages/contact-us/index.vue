<template>
    <Navbar />

    <div class="bg-custom-image bg-cover bg-center h-[620px] w-full text-white bg-transparent">
        <div class="mx-auto px-4">
            <div class="flex flex-col">






                <div class="flex items-center justify-center flex-grow pt-24">
                    <div class="text-center px-4 md:px-8">
                        <h1 class="text-2xl md:text-4xl font-bold mb-4">Contact Us</h1>
                        <p class="text-base md:text-lg">Get to discover our products and services tailored just for you.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>


    <div class="flex md:flex-row flex-col md:space-y-0 space-y-8 md:space-x-6 my-10 max-w-[800px] mx-auto items-center">
        <div
            class="flex flex-col my-auto bg-white border shadow-sm rounded-xl dark:bg-neutral-100 md:h-[400px] h-[300px] md:w-[500px] w-[250px] dark:border-neutral-300 dark:shadow-neutral-50/70">
            <div class="p-4 md:p-10  mx-auto my-auto">
                <div class="flex flex-col space-y-2 items-center">
                    <img src="/contact-us.svg" class="w-[80px] " alt="" srcset="">
                    <h3 class="text-[40px] font-bold text-gray-700 ">
                        Call us
                    </h3>
                </div>
                <p class="mt-2 text-gray-600 text-[20px] dark:text-neutral-400 text-center">
                    +1-917-6094-597
                </p>

            </div>
        </div>

        <div
            class="flex flex-col my-auto bg-white border shadow-sm rounded-xl dark:bg-neutral-100  md:h-[400px] h-[300px] md:w-[500px] w-[250px] dark:border-neutral-300 dark:shadow-neutral-50/70">
            <div class="p-4 md:p-10  mx-auto my-auto">
                <div class="flex flex-col space-y-2 items-center">
                    <img src="/location.svg" class="w-[80px] " alt="" srcset="">
                    <h3 class="text-[40px] font-bold text-gray-700 ">
                        Visit us
                    </h3>
                </div>
                <p class="mt-2 text-gray-600 text-[20px] dark:text-neutral-400 text-center">
                    USA, NewYork
                </p>

            </div>
        </div>

        <div
            class="flex flex-col my-auto bg-white border shadow-sm rounded-xl dark:bg-neutral-100  md:h-[400px] h-[300px] md:w-[500px] w-[250px] dark:border-neutral-300 dark:shadow-neutral-50/70">
            <div class="p-4 md:p-10  mx-auto my-auto">
                <div class="flex flex-col space-y-2 items-center">
                    <img src="/whatsapp.svg" class="w-[80px] " alt="" srcset="">
                    <h3 class="text-[40px] font-bold text-gray-700 ">
                        Mail us
                    </h3>
                </div>
                <p class="mt-2 text-gray-600 text-[20px] dark:text-neutral-400 text-center">
                    info@zemy-group.com
                </p>

            </div>
        </div>



    </div>


    <footer class="footer">
        <div class="container mx-auto py-6 px-4 flex flex-col md:flex-row items-center justify-between">
            <!-- Logo and Tagline -->
            <div class="text-center md:text-left">
                <img src="~/assets/images/bg2.png" alt="Company Logo" class="w-24 mb-2" />
                <p class="text-lg font-semibold">Innovating Solutions for Health & Aviation</p>
            </div>

            <!-- Navigation Links -->
            <nav class="mt-4 md:mt-0">
                <ul class="flex flex-col md:flex-row space-y-2 md:space-y-0 md:space-x-6">
                    <li>
                        <NuxtLink to="/" class="footer-link">Home</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/about" class="footer-link">About Us</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/services" class="footer-link">Services</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/contact" class="footer-link">Contact</NuxtLink>
                    </li>
                </ul>
            </nav>

            <!-- Contact Information -->
            <div class="mt-4 md:mt-0 text-center md:text-right">
                <p class="text-sm">147 W 35th st, NewYork, NY 10001</p>
                <p class="text-sm">+1(917)6094597</p>
                <p class="text-sm">Email: info@zemy-group.com</p>
            </div>
        </div>

        <!-- Bottom Bar -->
        <div class="mycol text-white text-center py-4 ">
            <p class="text-sm">© 2024 Zemy-group.cpm. All rights reserved.</p>
        </div>
    </footer>
</template>


<style>
.bg-custom-image {
    background-image: url("~/assets/images/aviation.jpg");
}

.mycol {
    background-color: rgb(158, 40, 41);
}
</style>

<script setup>
import Navbar from '~/layouts/navbar.vue';



</script>