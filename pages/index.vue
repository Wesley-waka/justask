<template>
  <nav class=" p-4">
    <div class="container mx-auto flex justify-between items-center">
      <NuxtLink to="/" class="text-gray-700 text-xl font-bold">
        <img src="~/assets/images/just-ask.svg" alt="Just Ask Logo" class="h-14">
      </NuxtLink>
      <div class="hidden md:flex space-x-4">
        <NuxtLink to="/" class="text-gray-700 hover:mycol">Home</NuxtLink>
        <NuxtLink to="/about-us" class="text-gray-700 hover:mycol">About</NuxtLink>
        <NuxtLink to="/services" class="text-gray-700 hover:mycol">Services</NuxtLink>
        <NuxtLink to="/contact" class="text-gray-700 hover:mycol">Contact</NuxtLink>
      </div>
      <button @click="isMenuOpen = !isMenuOpen" class="md:hidden text-gray-700 focus:outline-none">
        <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
        </svg>
      </button>
    </div>
    <div v-if="isMenuOpen" class="md:hidden mt-2">
      <NuxtLink to="/" class="block text-gray-700 py-2">Home</NuxtLink>
      <NuxtLink to="/about" class="block text-gray-700 py-2">About</NuxtLink>
      <NuxtLink to="/services" class="block text-gray-700 py-2">Services</NuxtLink>
      <NuxtLink to="/contact" class="block text-gray-700 py-2">Contact</NuxtLink>
    </div>
  </nav>
  <div class="grid grid-cols-1 md:grid-cols-2 h-full">
    <div class="flex items-center justify-center mycolor h-full">
      <h3 class="text-[28px] text-white font-bold text-center md:text-left">
        Sky-High Solutions for Health <br />&amp; Aviation Excellence
      </h3>
    </div>
    <div class="flex items-center justify-center h-full">
      <img src="~/assets/images/bg1.jpg" alt="Background Image" class="w-full h-auto object-cover">
    </div>
  </div>

  <div class="container mx-auto p-6">
    <h2 class="text-3xl font-bold mb-8 text-center">Our Services</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <div v-for="service in services" :key="service.id"
        class="service-card bg-cover bg-center bg-no-repeat rounded-lg shadow-lg overflow-hidden cursor-pointer"
        :style="{ backgroundImage: `url(https://images.pexels.com/photos/5778598/pexels-photo-5778598.jpeg)` }"
        @click="activeService = service">
        <div class="p-6 bg-white bg-opacity-70">
          <h3 class="text-xl font-semibold mb-2">{{ service.title }}</h3>
          <p class="text-gray-700">{{ service.description.slice(0, 100) }}...</p>
        </div>
        <div class="px-6 py-4 bg-white bg-opacity-70">
          <button class="mycol text-white hover:underline p-2 rounded-sm">Learn More</button>
        </div>
      </div>
    </div>

    <!-- Details of selected service -->
    <div v-if="activeService" class="mt-8 bg-gray-100 p-6 rounded-lg shadow-md">
      <h3 class="text-2xl font-semibold mb-4">{{ activeService.title }}</h3>
      <p class="text-gray-700">{{ activeService.description }}</p>
      <button @click="activeService = null" class="mt-4 mycol hover:underline">Close</button>
    </div>
  </div>
  <section class="bg-white py-16">
    <div class="container mx-auto px-4">
      <div class="flex flex-col lg:flex-row items-center">
        <!-- Text Content -->
        <div class="lg:w-1/2 mb-8 lg:mb-0 lg:pr-8">
          <h2 class="text-3xl font-semibold mb-4">About Our Company</h2>
          <p class="text-lg text-gray-700 mb-4">
            Our company is dedicated to providing top-notch services and solutions tailored to meet your needs. With a
            team of experienced professionals, we ensure that every project is handled with the utmost care and expertise.
          </p>
          <p class="text-lg text-gray-700">
            We specialize in delivering innovative solutions and exceptional customer service. Whether you’re looking for
            cutting-edge technology or reliable support, our team is here to help you succeed. Discover how we can make a
            difference for your business today.
          </p>
        </div>
        <!-- Image -->
        <div class="lg:w-1/2 ">
          <img src="https://images.pexels.com/photos/5778600/pexels-photo-5778600.jpeg" alt="Company Overview"
            class="w-full h-auto object-cover rounded-lg shadow-lg h-[400px]" />
        </div>
      </div>
    </div>
  </section>



  <div class="bg-gray-50 py-16">
    <div class="container mx-auto px-4">
      <h1 class="text-4xl font-semibold text-center mb-12">What Our Clients Say</h1>

      <!-- Testimonials Section -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Testimonial 1 -->
        <div class="bg-white p-6 rounded-lg shadow-lg text-center">
          <img src="https://images.pexels.com/photos/1006873/pexels-photo-1006873.jpeg" alt="Client 1"
            class="w-16 h-16 mx-auto mb-4 rounded-full object-cover" />
          <p class="text-lg text-gray-700 mb-4">
            "This company provided outstanding service and exceeded our expectations. Highly recommended!"
          </p>
          <h3 class="text-xl font-semibold">John Doe</h3>
          <p class="text-gray-500">CEO, Example Corp</p>
        </div>

        <!-- Testimonial 2 -->
        <div class="bg-white p-6 rounded-lg shadow-lg text-center">
          <img src="https://images.pexels.com/photos/1181716/pexels-photo-1181716.jpeg" alt="Client 2"
            class="w-16 h-16 mx-auto mb-4 rounded-full object-cover" />
          <p class="text-lg text-gray-700 mb-4">
            "A fantastic experience from start to finish. Their attention to detail is unmatched."
          </p>
          <h3 class="text-xl font-semibold">Jane Smith</h3>
          <p class="text-gray-500">Marketing Director, Sample Ltd</p>
        </div>

        <!-- Testimonial 3 -->
        <div class="bg-white p-6 rounded-lg shadow-lg text-center">
          <img src="https://images.pexels.com/photos/207383/pexels-photo-207383.jpeg" alt="Client 3"
            class="w-16 h-16 mx-auto mb-4 rounded-full object-cover" />
          <p class="text-lg text-gray-700 mb-4">
            "Exceptional quality and service. They truly care about their clients and it shows."
          </p>
          <h3 class="text-xl font-semibold">Emily Johnson</h3>
          <p class="text-gray-500">Product Manager, Demo Co</p>
        </div>
      </div>
    </div>
  </div>

  <div class="gallery-container px-8">
    <h2 class="font-bold text-2xl flex justify-center p-4">Gallery</h2>
    <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-3 gap-4">
      <div v-for="(image, index) in images" :key="index" class="thumbnail-wrapper" @click="openModal(index)">
        <img :src="image.thumbnail" :alt="`Thumbnail of ${image.alt}`" class="thumbnail" />
      </div>
    </div>

    <!-- Modal for Larger Image -->
    <div v-if="modalOpen" class="modal-overlay" @click="closeModal">
      <div class="modal-content" @click.stop>
        <img :src="images[activeImageIndex].full" :alt="`Full size of ${images[activeImageIndex].alt}`"
          class="full-image" />
        <button @click="closeModal" class="close-button">✕</button>
      </div>
    </div>
  </div>

  <div class="bg-gray-50 py-16">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-semibold text-center mb-12">Contact Us</h2>
      <form @submit.prevent="handleSubmit" class="max-w-lg mx-auto bg-white p-8 rounded-lg shadow-lg">
        <div class="mb-4">
          <label for="name" class="block text-gray-700 text-sm font-medium mb-2">Name</label>
          <input v-model="form.name" type="text" id="name" placeholder="Your Name"
            class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:mycol"
            required />
        </div>
        <div class="mb-4">
          <label for="email" class="block text-gray-700 text-sm font-medium mb-2">Email</label>
          <input v-model="form.email" type="email" id="email" placeholder="Your Email"
            class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:mycol"
            required />
        </div>
        <div class="mb-4">
          <label for="message" class="block text-gray-700 text-sm font-medium mb-2">Message</label>
          <textarea v-model="form.message" id="message" placeholder="Your Message" rows="4"
            class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:mycol"
            required></textarea>
        </div>
        <button type="submit"
          class="w-full mycol text-white py-2 px-4 rounded-md hover:mycol focus:outline-none focus:ring-2 focus:mycol">
          Send Message
        </button>
      </form>
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
const isMenuOpen = ref(false)

const services = [
  {
    id: 'aviation',
    title: 'Aviation Consulting',
    description: `Just ASK LLC provides comprehensive consulting services in the aviation industry. 
    We offer aircraft sales, services, and spares across various manufacturers. 
    With a focus on high-growth regions such as Asia and Africa, we aim to support the 
    nascent aviation industry by providing bespoke solutions tailored to the needs of these 
    emerging markets. Our experience of over 25 years ensures that we deliver expert advice 
    and reliable solutions to our clients.`
  },
  {
    id: 'health',
    title: 'Health Foods Consulting',
    description: `We specialize in health-related food products, including organic foods, alkaline salts, 
    and healthy sugars. With rising costs in healthcare, we advocate for prevention through 
    healthy food intake to promote better health. We focus on combating major health issues 
    like diabetes and high blood pressure by offering products that contribute to a healthier lifestyle.`
  },
  {
    id: 'expansion',
    title: 'Global Expansion & Support',
    description: `Our mission is to expand our presence in the rapidly growing aviation markets of 
    Asia and Africa. We are committed to supporting underprivileged areas by offering tailored 
    solutions in both health and aviation fields. Our goal is to provide bespoke services that 
    address the unique challenges faced by these regions, leveraging our extensive industry experience.`
  },
];

const activeService = ref(null);

const images = [
  {
    thumbnail: 'https://images.pexels.com/photos/5778600/pexels-photo-5778600.jpeg',
    full: 'https://images.pexels.com/photos/5778600/pexels-photo-5778600.jpeg',
    alt: 'Aircraft'
  },
  {
    thumbnail: 'https://images.pexels.com/photos/13404732/pexels-photo-13404732.jpeg',
    full: 'https://images.pexels.com/photos/13404732/pexels-photo-13404732.jpeg',
    alt: 'Aircraft'
  },
  {
    thumbnail: 'https://images.pexels.com/photos/13404726/pexels-photo-13404726.jpeg',
    full: 'https://images.pexels.com/photos/13404726/pexels-photo-13404726.jpeg',
    alt: 'Aircraft'
  },
  {
    thumbnail: 'https://images.pexels.com/photos/12692959/pexels-photo-12692959.jpeg',
    full: 'https://images.pexels.com/photos/12692959/pexels-photo-12692959.jpeg',
    alt: 'Aircraft'
  },
  {
    thumbnail: 'https://images.pexels.com/photos/63991/pexels-photo-63991.jpeg',
    full: 'https://images.pexels.com/photos/63991/pexels-photo-63991.jpeg',
    alt: 'Aircraft'
  },
  {
    thumbnail: 'https://images.pexels.com/photos/13404721/pexels-photo-13404721.jpeg',
    full: 'https://images.pexels.com/photos/13404721/pexels-photo-13404721.jpeg',
    alt: 'Aircraft'
  },
];

const modalOpen = ref(false);
const activeImageIndex = ref(null);

const openModal = (index) => {
  activeImageIndex.value = index;
  modalOpen.value = true;
}

const closeModal = () => {
  modalOpen.value = false;
  activeImageIndex.value = null;
}
import { ref } from 'vue';

const form = ref({
  name: '',
  email: '',
  message: ''
});

const handleSubmit = () => {
  // Here, you would typically handle the form submission.
  // This could involve sending the form data to an API or a server.
  console.log('Form submitted:', form.value);

  // Clear form after submission (optional)
  form.value = {
    name: '',
    email: '',
    message: ''
  };
};
</script>

<style>
.mycolor {
  background-color: rgb(0, 169, 245);
}

.service-card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.service-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
}

.service-card .text-gray-700 {
  line-clamp: 2;
  /* Limit text to two lines */
  overflow: hidden;
  text-overflow: ellipsis;
}

.footer {
  background-color: #f8f9fa;
  color: #343a40;
}

.footer-link {
  text-decoration: none;
  color: #007bff;
}

.footer-link:hover {
  text-decoration: underline;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.mycol {
  background-color: rgb(158, 40, 41);
}

@media (max-width: 768px) {
  .footer {
    padding: 1rem;
  }
}
</style>