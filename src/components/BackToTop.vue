<template>
  <button
    v-if="isVisible"
    @click="scrollToTop"
    class="fixed bottom-4 z-[99999] right-4 bg-(--color-secondaryalt) text-white rounded-full w-12 h-12 flex items-center justify-center text-xl cursor-pointer transition-opacity duration-300 hover:bg-(--color-secondaryalt)"
  >
    <ArrowUpCircleIcon class="w-full h-full text-white" />
  </button>
</template>
<script setup>
import { ArrowUpCircleIcon } from "@heroicons/vue/16/solid";
import { ref, onMounted, onUnmounted } from "vue";

const isVisible = ref(false);
const handleScroll = () => {
  isVisible.value = window.scrollY > 300;
};
const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: "smooth" });
};
onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});
onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>
