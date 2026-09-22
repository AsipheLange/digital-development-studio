<script setup>
import {
  ArrowRight,
  MessageSquare,
} from '@lucide/vue'
</script>

<template>
  <section class="relative overflow-hidden bg-[#111827] py-20 lg:py-24">

    <!-- Decorative background -->
    <div
      class="absolute -left-32 -top-32 h-72 w-72 rounded-full bg-[#635BFF]/20 blur-3xl"
    ></div>

    <div
      class="absolute -bottom-32 -right-32 h-72 w-72 rounded-full bg-[#14B8A6]/20 blur-3xl"
    ></div>

    <div class="relative mx-auto max-w-4xl px-6 text-center lg:px-8">

      <!-- Icon -->
      <div
        class="mx-auto flex h-14 w-14 items-center justify-center rounded-2xl bg-white/10 text-[#14B8A6]"
      >
        <MessageSquare :size="25" :stroke-width="1.8" />
      </div>

      <!-- Eyebrow -->
      <p
        class="mt-6 text-sm font-semibold uppercase tracking-wider text-[#14B8A6]"
      >
        Start your project
      </p>

      <!-- Heading -->
      <h2
        class="mt-4 text-3xl font-bold tracking-tight text-white sm:text-4xl lg:text-5xl"
      >
        Have a project in mind?
        <span class="text-[#635BFF]">
          Let's build it.
        </span>
      </h2>

      <!-- Description -->
      <p
        class="mx-auto mt-6 max-w-2xl text-lg leading-8 text-gray-300"
      >
        Tell us what you're trying to achieve, and let's explore
        the right digital solution for your business.
      </p>

      <!-- Buttons -->
      <div class="mt-8 flex flex-col justify-center gap-4 sm:flex-row">

        <RouterLink
          to="/contact"
          class="group inline-flex items-center justify-center rounded-xl bg-white px-6 py-3.5 font-semibold text-[#111827] transition hover:bg-[#635BFF] hover:text-white"
        >
          Start a Project

          <ArrowRight
            class="ml-2 transition-transform group-hover:translate-x-1"
            :size="18"
          />
        </RouterLink>

        <RouterLink
          to="/work"
          class="inline-flex items-center justify-center rounded-xl border border-white/20 px-6 py-3.5 font-semibold text-white transition hover:border-[#14B8A6] hover:text-[#14B8A6]"
        >
          See My Work
        </RouterLink>

      </div>

      <!-- Supporting text -->
      <p class="mt-6 text-sm text-gray-400">
        Websites · Web Applications · E-Commerce · Business Systems
      </p>

    </div>
  </section>
</template>