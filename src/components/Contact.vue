<template>
  <section class="relative py-20 overflow-hidden" id="contact">
    <div class="relative z-10 max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center m-16" data-aos="fade-up">
        <h2 class="text-4xl md:text-5xl font-bold text-(--color-text) mb-4">
          Get In
          <span
            class="text-transparent bg-clip-text bg-linear-to-r from-[#b14aed] to-[#454ade]"
          >
            Touch
          </span>
        </h2>
        <p class="text-(--color-text) text-lg">
          Let's Work Together On Your Next Project
        </p>
      </div>

      <div class="grid lg:grid-cols-2 gap-12">
        <div data-aos="fade-right">
          <h3 class="text-3xl font-bold text-(--color-text) mb-6">
            Contact Information
          </h3>
          <div class="space-y-14">
            <div class="flex items-center gap-3">
              <EnvelopeIcon class="w-6 h-6 text-(--color-text)" />
              <div>
                <p class="text-(--color-text) font-semibold">Email</p>
                <p class="text-(--color-text)">ian.garnett@hotmail.com</p>
              </div>
            </div>

            <div class="flex justify-items-center gap-2">
              <img :src="githuboutline" class="w-7 h-5 bg-black text-(--color-text)" />
              <div>
                <p class="text-(--color-text) font-semibold">GitHub</p>
                <a
                  href="https://github.com/ttPuck"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="text-(--color-secondary) hover:text-cyan-400 transition-colors"
                >
                  ttPuck
                </a>
              </div>
            </div>
          </div>
        </div>

        <!-- FORM -->
        <div data-aos="fade-left">
          <form
            class="space-y-6"
            action="mailto:ian.garnett@hotmail.com"
            method="GET"
          >
            <div class="grid sm:grid-cols-2 gap-6">
              <div>
                <label class="text-(--color-text) text-sm font-medium mb-2 block">
                  Name
                </label>
                <input
                  type="text"
                  name="name"
                  class="w-full bg-gray-500/20 border border-[#5386e4] rounded-xl px-4 py-3 text-(--color-text)"
                />
              </div>

              <div>
                <label class="text-(--color-text) text-sm font-medium mb-2 block">
                  Email
                </label>
                <input
                  type="email"
                  name="email"
                  class="w-full bg-gray-500/20 border border-[#5386e4] rounded-xl px-4 py-3 text-(--color-text)"
                />
              </div>

              <div>
                <label class="text-(--color-text) text-sm font-medium mb-2 block">
                  Subject
                </label>
                <input
                  type="text"
                  name="subject"
                  class="w-full bg-gray-500/20 border border-[#5386e4] rounded-xl px-4 py-3 text-(--color-text)"
                />
              </div>
            </div>

            <div>
              <label class="text-(--color-text) text-sm font-medium mb-2 block">
                Message
              </label>
              <textarea
                name="body"
                rows="5"
                class="w-full bg-gray-500/20 border border-[#5386e4] rounded-xl px-4 py-3 text-(--color-text)"
              ></textarea>
            </div>

            <button
              type="submit"
              class="w-full bg-(--color-primaryalt) hover:bg-(--color-secondary) cursor-pointer text-white font-semibold py-3 rounded-xl"
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
import { EnvelopeIcon } from "@heroicons/vue/16/solid";
import githuboutline from "../../public/github-outline.png";
</script>
