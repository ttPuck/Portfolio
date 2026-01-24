<template>
  <section class="relative py-20 overflow-hidden" id="contact">
    <div class="relative z-10 max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center m-16" data-aos="fade-up">
        <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
          Get In
          <span
            class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 to-cyan-400"
          >
            Touch
          </span>
        </h2>
        <p class="text-white text-lg">
          Let's Work Together On Your Next Project
        </p>
      </div>
      <div class="grid lg:grid-cols-2 gap-12">
        <div data-aos="fade-right">
          <h3 class="text-2xl font-bold text-white mb-6">
            Contact Information
          </h3>
          <div class="space-y-6">
            <div class="flex items-center gap-4 ">
              <EnvelopeIcon class="w-6 h-6 text-blue-400" />
              <div>
                <p class="text-white font-semibold">Email</p>
                <p class="text-white">ian.garnett@hotmail.com</p>
              </div>
            </div>
            <div class="flex justify-items-center gap-3">
              <img :src="githuboutline" class="w-10 h-7 text-blue-400" />
              <div>
                <p class="text-white font-semibold">Github</p>
                <a
                  href="https://github.com/ptwees"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="text-orange-300 hover:text-cyan-400 transition-colors"
                >
                  ptwees
                </a>
              </div>
            </div>
            <div class="flex items-center gap-4">
            </div>
          </div>
          
        </div>
        <div data-aos="fade-left">
          <form class="space-y-6">
            <div class="grid sm:grid-cols-2 gap-6">
              <div>
                <label class="text-white text-sm font-medium mb-2 block">
                  Name
                </label>
                <input
                  type="text"
                  class="w-full bg-gray500/20 border border-[#5386e4] rounded-xl px-4 py-3 text-white placeholder-blue-400 focus:border-cyan-200 focus:outline-none transition-all"
                />
              </div>
              <div>
                <label class="text-white text-sm font-medium mb-2 block">
                  Email
                </label>
                <input
                  type="email"
                  class="w-full bg-gray500/20 border border-[#5386e4] rounded-xl px-4 py-3 text-white placeholder-blue-400 focus:border-cyan-200 focus:outline-none transition-all"
                />
              </div>
              <div>
                <label class="text-white text-sm font-medium mb-2 block">
                  Subject
                </label>
                <input
                  type="text"
                  class="w-full bg-gray500/20 border border-[#5386e4] rounded-xl px-4 py-3 text-white placeholder-blue-400 focus:border-cyan-200 focus:outline-none transition-all"
                />
              </div>
            </div>
            <div>
              <label class="text-white text-sm font-medium mb-2 block">
                Message
              </label>
              <textarea
                rows="5"
                class="w-full bg-gray500/20 border border-[#5386e4] rounded-xl px-4 py-3 text-white placeholder-blue-400 focus:border-cyan-200 focus:outline-none transition-all"
              >
              </textarea>
            </div>
            <button
              type="submit"
              class="w-full bg-linear-to-r from-[#5386e4] to-cyan-500 text-white font-semibold py-3 rounded-xl hover:shadow-lg hover:shadow-[#b14aed]/60 transition-all duration-300"
            >
              Send Message
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
import {
  EnvelopeIcon,
} from "@heroicons/vue/16/solid";

import githuboutline from "../../public/github-outline.png";
</script>
