<template>
  <section class="relative py-20 overflow-hidden" id="testimonials">
    <div class="relative z-10 max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16" data-aos="fade-up">
        <h2
          class="text-4xl md:text-5xl font-bold text-white"
          data-aos="fade-up"
        >
          Client
          <span
            class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 to-cyan-400"
          >
            Testimonials
          </span>
        </h2>
        <p class="text-blue-200 text-lg">
          What people say about working with me
        </p>
      </div>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-5 lg:grid-cols-3 gap-6">
        <div
          v-for="(testimonial, index) in testimonials"
          :key="testimonial.id"
          class="bg-linear-to-br from-gray-800/50 to-blue-900/30 rounded-2xl p-6 border border-blue-500/20 backdrop-blur-sm hover:border-blue-400 transition-all duration-300"
          data-aos="fade-up"
          :data-aos-delay="index * 100"
        >
          <div class="flex gap-1 mb-4">
            <StarIcon v-for="n in 5" :key="n" class="w-5 h-5 text-yellow-400" />
          </div>
          <p class="text-blue-100 text-sm leading-relaxed mb-6">
            "{{ testimonial.text }}"
          </p>
          <div class="flex items-center gap-4">
            <div
              class="w-12 h-12 rounded-full overflow-hidden border-2 border-blue-400/50"
            >
              <img
                :src="testimonial.avatar"
                :alt="testimonial.name"
                class="w-full h-full object-cover"
              />
            </div>
            <div>
              <p class="text-white font-semibold">
                {{ testimonial.name }}
              </p>
              <p class="text-blue-300 text-sm">
                {{ testimonial.position }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
import { StarIcon } from "@heroicons/vue/16/solid";
import person1 from "../../public/person1.png";
import person2 from "../../public/person2.png";
import person3 from "../../public/person3.png";
const testimonials = [
  {
    id: 1,
    text: `The LORD said to my Lord, 
        “Sit in the place of honor at my right hand 
        until I humble your enemies, making them a 
        footstool under your feet."`,
    name: "Alex Garbero",
    position: "CEO, Garbero Media",
    avatar: person1,
  },
  {
    id: 2,
    text: `The LORD said to my Lord, 
        “Sit in the place of honor at my right hand 
        until I humble your enemies, making them a 
        footstool under your feet."`,
    name: "Alex Garbero",
    position: "Product Manager",
    avatar: person2,
  },
  {
    id: 3,
    text: `The LORD said to my Lord, 
        “Sit in the place of honor at my right hand 
        until I humble your enemies, making them a 
        footstool under your feet."`,
    name: "Alex Garbero",
    position: "CEO, Garbero Media",
    avatar: person3,
  },
];
</script>
