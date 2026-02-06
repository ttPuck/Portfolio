<template>
  <section class="relative py-20 overflow-hidden" id="testimonials">
    <div class="relative z-10 max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16" data-aos="fade-up">
        <h2
          class="text-4xl md:text-5xl font-bold text-black"
          data-aos="fade-up"
        >
          Client
          <span
            class="text-transparent bg-clip-text bg-linear-to-r from-[#b14aed] to-[#454ade]"
          >
            Testimonials
          </span>
        </h2>
        <p class="text-white text-lg">
          What People Say About Working With Me
        </p>
      </div> 
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-6">
        <div
          v-for="(testimonial, index) in testimonials"
          :key="testimonial.id"
          class="bg-(--color-secondaryalt) rounded-2xl p-6 border border-blue-500/20 backdrop-blur-sm hover:border-blue-400 transition-all duration-300"
          data-aos="fade-up"
          :data-aos-delay="index * 100"
        >
          <div class="flex gap-1 mb-4">
            <StarIcon v-for="n in 5" :key="n" class="w-5 h-5 text-yellow-400" />
          </div>
          <p class="text-white text-sm leading-relaxed mb-6">
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
              <p class="text-(--color-sidealt) text-sm">
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
    text: `Ian has an admirable level of attention to detail, 
    and a profound ability to comprehend complex subjects quickly. His creativity 
    and adaptability to problems is limitless, and it shows in the projects he has produced.
     Ian is a wonderful person to work with, and I would recommend him to anyone interested in an extraordinary team player.`,
    name: "Alex Garbero",
    position: "CEO, Garbero Media",
    avatar: person3,
  },
  {
    id: 2,
    text: `Able to understand and comprehend any and all ideas brought to him, Ian is able to deliver a finalized product to 
    clients on time and well above
    their expectations. His ability to distill and explain overly technical ideas and topics to any person is amazing in a team
    environment. Ian delivers amazing products with end users in mind and is a creative powerhouse.`,
    name: "Faith Talent Services",
    position: "Recruiting Business",
    avatar: person2,
  },
];
</script>
