<script setup lang="ts">
import Button from "./ui/button/Button.vue";

const links = [
  { name: "About", to: "/about" },
  { name: "Shop", to: "/shop" },
  { name: "Contact", to: "/contact" },
];
</script>

<template>
  <footer class="bg-secondary text-primary py-8">
    <div class="container mx-auto px-6">
      <div class="flex flex-wrap justify-between">
        <div class="w-full md:w-1/3 mb-6 md:mb-0">
          <h3 class="text-xl font-semibold mb-2">Perfumest</h3>
          <p class="text-gray-400">Your destination for fine fragrances</p>
        </div>
        <div class="w-full md:w-1/3 mb-6 md:mb-0">
          <h3 class="text-xl font-semibold mb-2">Quick Links</h3>
          <ul class="text-gray-400">
            <li v-for="link in links">
              <RouterLink :to="link.to">{{ link.name }}</RouterLink>
            </li>
          </ul>
        </div>
        <div class="w-full md:w-1/3">
          <h3 class="text-xl font-semibold mb-2">Stay Connected</h3>
          <p class="text-gray-400 mb-2">
            Subscribe to our newsletter for exclusive offers
          </p>
          <form class="flex h-10">
            <input
              type="email"
              placeholder="Your email"
              class="bg-gray-700 text-white px-4 py-2 rounded-l-full focus:outline-none"
            />
            <Button
              type="submit"
              class="h-full text-white px-4 py-2 rounded-r-full transition duration-300"
            >
              Subscribe
            </Button>
          </form>
        </div>
      </div>
      <div
        class="border-t border-gray-700 700 mt-8 pt-8 text-center text-gray-300"
      >
        <p>&copy; 2024 Perfumest. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>
