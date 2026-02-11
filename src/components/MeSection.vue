<template>
  <section
    class="relative w-full overflow-hidden min-h-50px flex items-center"
  >
    <div
      class="min-w-screen px-3 sm:px-5 md:px-8 lg:px-12 max-w-5xl lg:max-w-6xl mx-auto relative z-10"
    >
      <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 items-center">
        <!-- Profile Image-->
        <div class="lg:min-h-20px flex justify-center">
          <div class="relative w-100 max-w-md lg:max-w-lg">
            <div
              class="relative z-10 border-pulse bg-linear-to-r from-(--color-side) to-(--color-primary) shadow-2xl rounded-[10%_10%_10%_15%/10%_10%_10%_10%] p-4 backdrop-blur-sm -translate-y-6"
              data-aos="zoom-in"
              data-aos-delay="450"
            >
              <div class="rounded-xl overflow-hidden">
                <img
                  src="../../public/Ian.png"
                  alt="Ian - Profile Image"
                  loading="lazy"
                  class="w-[300px] h-[300px] object-contain -translate-y-3 translate-x-8 rounded-[20%]"
                />
              </div>
            </div>
          </div>
        </div>
        <div class="flex flex-col md:mt-0 mt-20 justify-center">
          <div class="text-white lg:text-center" data-aos="fade-right">
            <h1
              class="text-white font-bold text-2xl md:text-3xl lg:text-4xl leading-tight"
            >
              Welcome, My Name Is
              <span
                class="text-transparent bg-clip-text bg-linear-to-r from-[#b14aed] to-[#454ade]"
                >Ian </span
              >
            </h1>
            <p
              class="text-white font-medium text-lg md:text-xl mt-4"
              data-aos="fade-right"
              data-aos-delay="80"
            ></p>
            <p>Full-Stack Developer</p>
          </div>
          <p
            class="font-light text-white pt-4 text-center lg:text-center mx-auto max-w-xl text-lg leading-relaxed"
            data-aos="fade-right"
            data-aos-delay="150"
          >
            I am an experienced frontend and backend developer of 2+ years, with
            a handful of projects under my belt. I specialize in JavaScript and
            its extended frameworks like React, Next.js and Vue.js, along with
            their complementary backend tools such as MongoDB, Supabase, and
            Cloudflare. I would love to be part of a team where I could deliver
            effective and efficient code and provide my gifts and skills to any
            project that may need them!
          </p>
          <div
    class="flex items-end gap-4 pt-8 flex-col sm:flex-row w-full justify-center lg:justify-center"
            data-aos="fade-up"
            data-aos-delay="450"
          >
            <div
              class="p-[2px] bg-linear-to-r from-(--color-side) to-(--color-secondary) rounded-xl w-full sm:w-max"
            >
              <button
                @click="scrollToContact"
                class="px-8 md:px-10 py-4 rounded-xl relative group w-full sm:w-max flex justify-center overflow-hidden bg-(--color-side) hover:bg-(--color-secondary) cursor-pointer transition-all duration-300"
              >
                <span
                  class="relative flex items-center justify-center text-white font-semibold text-lg"
                >
                  Reach out to me
                  <ArrowRightIcon
                    class="ml-2 w-5 h-5 group-hover:translate-x-1 transition-transform"
                  />
                </span>
              </button>
            </div>
            <a href="/Ian.Portfolio.pdf" download>
              <!-- Gradient wrapper -->
              <div
                class="p-[2px] bg-linear-to-r from-(--color-side) to-(--color-secondary) rounded-xl w-full sm:w-max"
              >
                <!-- Inner button -->
                <button
                  class="px-8 md:px-10 py-4 rounded-xl relative group w-full flex justify-center bg-(--color-side) hover:bg-(--color-secondary) transition-all duration-300"
                >
                  <div
                    class="flex items-center justify-center relative cursor-pointer"
                  >
                    <ArrowDownTrayIcon
                      class="w-5 h-5 text-white group-hover:translate-y-1 transition-transform"
                    />
                    <span class="pl-3 text-white font-semibold text-lg">
                      Download CV
                    </span>
                  </div>
                </button>
              </div>
            </a>
          </div>
          <div
            class="flex items-center justify-center lg:justify-center gap-7 pt-12"
            data-aos="fade-up"
            data-aos-delay="300"
          >
            <div class="text-center">
              <div class="text-2xl font-bold text-white">4</div>
              <div class="text-white text-sm">Projects</div>
            </div>
            <div class="text-center">
              <div class="text-2xl font-bold text-white">2+</div>
              <div class="text-white text-sm">Years</div>
            </div>
            <div class="text-center">
              <div class="text-2xl font-bold text-white">2+</div>
              <div class="text-white text-sm">Clients</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import {
  ArrowDownTrayIcon,
  ArrowRightIcon,
} from "@heroicons/vue/16/solid";
import { ref } from "vue";
const scrollToContact = () => {
  const el = document.getElementById("contact");
  if (!el) return;
  el.scrollIntoView({ behavior: "smooth" });
};
</script>
