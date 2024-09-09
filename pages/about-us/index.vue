<template>
    <Navbar />

    <div class="bg-custom-image bg-cover bg-center h-[720px] text-white bg-transparent">
        <div class="mx-auto px-4">
            <div class="flex flex-col">
                <div class="flex items-center h-16 bg-transparent relative z-20">
                    <div class="md:hidden flex items-center">
                        <button @click="toggleMenu" class="text-white focus:outline-none bg-transparent z-30">
                            <i class="pi pi-bars text-2xl"></i>
                        </button>
                    </div>



                </div>


                <div class="flex items-center justify-center flex-grow pt-24">
                    <div class="text-center px-4 md:px-8">
                        <h1 class="text-2xl leading-[90px] md:text-[80px] font-bold mb-4">LUXURY ABOVE AND <br>BEYOND THE
                            RUNWAY
                        </h1>
                        <!-- <p class="text-base md:text-lg">Get to discover our products and services tailored just for you.</p> -->
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="bg-slate-100">
        <div class="max-w-[100rem]  mx-auto px-6">
            <div class="flex lg:flex-row flex-col items-center bg-slate-100">
                <div>
                    <h1 class="text-[70px] font-semibold">Nutritious Meal Options</h1>
                    <p class="md:w-[600px]">We believe that healthy eating should be accessible to everyone. Our range of
                        meal options includes organic, locally sourced ingredients designed to boost energy and enhance
                        well-being. From grab-and-go snacks to full-course meals, we cater to various dietary needs,
                        including vegan, gluten-free, and low-calorie choices.</p>
                </div>
                <img src="~/assets/images/unbg-1.png" alt="" class='w-[1400px]' srcset="">
            </div>
        </div>
    </div>

    <div style="background-color: rgb(158, 40, 41);">
        <div class="max-w-[110rem]  mx-auto px-6">
            <div class="flex lg:flex-row flex-col-reverse  py-[60px] text-white items-center">
                <img src="~/assets/images/food.png" class='w-[900px]' alt="">
                <div>
                    <div>
                        <h1 class="text-[70px]">Good Food,</h1>
                        <div class="p-3 bg-white rounded-full text-center mx-[80px] w-[15px]"></div>
                        <h1 class="text-[70px]"> Good Life</h1>
                        <p class="md:w-[600px]">Understanding that every individual has unique nutritional requirements, we
                            offer tailored meal plans for organizations, including airlines and corporate clients. Our
                            nutritionists work closely with you to create menus that meet specific health goals while
                            satisfying diverse tastes.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>




    <div class="bg-slate-100">
        <div class="max-w-[100rem]  mx-auto">
            <div class="flex lg:flex-row flex-col items-center bg-slate-100">
                <div>
                    <h1 class="text-[70px] font-semibold">Sustainable Practices</h1>
                    <p class="md:w-[600px] w-[400px]">Our commitment to sustainability extends to our food sourcing and
                        packaging. We prioritize eco-friendly practices that reduce waste and support local farmers,
                        ensuring that every meal is not only healthy but also kind to the planet.</p>
                </div>
                <img src="~/assets/images/unbg-2.png" alt="" class='w-[1000px]' srcset="">
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

<script setup>
import Navbar from '~/layouts/navbar.vue';

</script>


<style scoped>
/* .container {
    background-image: url("@/assets/images/about1.jpg");
} */

.bg-custom-image {
    background-image: url("~/assets/images/aviation.jpg");
}

.mycol {
    background-color: rgb(158, 40, 41);
}
</style>