<template>
  <header
    class="flex justify-between items-center p-6 bg-(--color-nav) relative z-20"
    id="home"
  >
    <div class="text-3xl text-(--color-text)">
      Web Dev <span class="font-bold text-(--color-side)">Portfolio</span>
    </div>
    <div class="md:hidden z-30">
      <button
        type="button"
        class="block focus:outline-none p-2 rounded-lg bg-(--color-side) hover:bg-(--color-secondary) transition-all duration-300"
        @click="isMenuOpen = !isMenuOpen"
      >
        <div class="relative w-6 h-6">
          <span
            :class="[
              `absolute left-0 w-6 h-0.5 bg-blue-200 transition-all
        duration-300`,
              isMenuOpen ? 'rotate-45 top-3' : 'top-1',
            ]"
          ></span>
          <span
            :class="[
              `absolute left-0 w-6 h-0.5 bg-blue-200 transition-all
        duration-300`,
              isMenuOpen ? 'opacity-0' : 'top-3 opacity-100',
            ]"
          ></span>
          <span
            :class="[
              `absolute left-0 w-6 h-0.5 bg-blue-200 transition-all
        duration-300`,
              isMenuOpen ? 'rotate-45 top-3' : 'top-5',
            ]"
          ></span>
        </div>
      </button>
    </div>
    <nav
      :class="[
        `fixed inset-0 z-20 flex flex-col items-center justify-center
    bg-(--color-bg) md:relative md:bg-transparent md:flex
    md:justify-between md:flex-row`,
        isMenuOpen ? 'block' : 'hidden',
      ]"
    >
      <ul
        class="flex flex-col items-center space-y-5 md:flex-row md:space-x-5 md:space-y-0"
      >
        <li v-for="item in Menu" :key="item.name" class="group relative">
          <a
            :href="item.href"
            class="relative block text-(--color-text) hover:text-(--color-secondary) transition-all duration-300 text-xl md:text-base font-medium group"
            @click="scrollToSection(item.href)"
          >
            {{ item.name }}
            <span
              class="absolute bottom-0 left-0 w-0 h-0.5 bg-(--color-head) transition-all duration-300 group-hover:w-full"
            ></span>
          </a>
        </li>
      </ul>
      <div class="mt-8 md:mt-0 md:ml-8">
        <button
          @click="scrollToContact"
          class="px-6 py-2.5 bg-(--color-secondary) cursor-pointer text-(--color-text) rounded-full hover:shadow-lg hover:shadow-[#b14aed]/60 transition-all duration-300 hover:scale-105"
        >
          Message Me!
        </button>
      </div>
    </nav>
  </header>
</template>
<script setup>
import { ref } from "vue";
const Menu = ref([
  { name: "Projects", href: "#projects" },
  { name: "Services", href: "#services" },
  { name: "About", href: "#about" },
  { name: "Skillset", href: "#skillset" },
  { name: "Testimonials", href: "#testimonials" },
]);
const isMenuOpen = ref(false);
const scrollToContact = () => {
  const el = document.getElementById("contact");
  if (!el) return;

  el.scrollIntoView({ behavior: "smooth" });
};
const scrollToSection = (href) => {
  isMenuOpen.value = false;
  const section = document.querySelector(href);
  if (section) {
    section.scrollIntoView({ behavior: "smooth" });
  }
};
</script>
