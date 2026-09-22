<script setup>
import { ref } from 'vue'
import { Menu, X } from '@lucide/vue'

const isMenuOpen = ref(false)

const closeMenu = () => {
  isMenuOpen.value = false
}
</script>

<template>
  <header class="sticky top-0 z-50 border-b border-[#E5E7EB] bg-white/95 backdrop-blur">
    <nav class="mx-auto flex max-w-7xl items-center justify-between px-6 py-4 lg:px-8">

      <!-- Logo -->
      <RouterLink
        to="/"
        class="flex items-center gap-3"
        @click="closeMenu"
      >
        <div
          class="flex h-10 w-10 items-center justify-center rounded-xl bg-[#635BFF] font-bold text-white"
        >
          DD
        </div>

        <div class="hidden sm:block">
          <p class="text-sm font-bold text-[#111827]">
            Digital Development
          </p>

          <p class="text-xs text-[#6B7280]">
            Studio
          </p>
        </div>
      </RouterLink>

      <!-- Desktop Navigation -->
      <div class="hidden items-center gap-8 md:flex">

        <RouterLink
          to="/"
          class="text-sm font-medium text-[#6B7280] transition hover:text-[#635BFF]"
          active-class="!text-[#635BFF]"
        >
          Home
        </RouterLink>

        <RouterLink
          to="/services"
          class="text-sm font-medium text-[#6B7280] transition hover:text-[#635BFF]"
          active-class="!text-[#635BFF]"
        >
          Services
        </RouterLink>

        <RouterLink
          to="/work"
          class="text-sm font-medium text-[#6B7280] transition hover:text-[#635BFF]"
          active-class="!text-[#635BFF]"
        >
          Work
        </RouterLink>

        <RouterLink
          to="/about"
          class="text-sm font-medium text-[#6B7280] transition hover:text-[#635BFF]"
          active-class="!text-[#635BFF]"
        >
          About
        </RouterLink>

        <RouterLink
          to="/contact"
          class="rounded-lg bg-[#111827] px-5 py-2.5 text-sm font-semibold text-white transition hover:bg-[#635BFF]"
        >
          Start a Project
        </RouterLink>

      </div>

      <!-- Mobile Menu Button -->
      <button
        class="flex h-10 w-10 items-center justify-center rounded-lg border border-[#E5E7EB] text-[#111827] transition hover:border-[#635BFF] hover:text-[#635BFF] md:hidden"
        aria-label="Toggle menu"
        :aria-expanded="isMenuOpen"
        @click="isMenuOpen = !isMenuOpen"
      >
        <X v-if="isMenuOpen" :size="22" />
        <Menu v-else :size="22" />
      </button>

    </nav>

    <!-- Mobile Navigation -->
    <div
      v-if="isMenuOpen"
      class="border-t border-[#E5E7EB] bg-white px-6 py-5 md:hidden"
    >
      <div class="flex flex-col gap-2">

        <RouterLink
          to="/"
          class="rounded-lg px-3 py-3 text-sm font-medium text-[#111827] transition hover:bg-[#F8F9FB] hover:text-[#635BFF]"
          active-class="bg-[#F8F9FB] !text-[#635BFF]"
          @click="closeMenu"
        >
          Home
        </RouterLink>

        <RouterLink
          to="/services"
          class="rounded-lg px-3 py-3 text-sm font-medium text-[#111827] transition hover:bg-[#F8F9FB] hover:text-[#635BFF]"
          active-class="bg-[#F8F9FB] !text-[#635BFF]"
          @click="closeMenu"
        >
          Services
        </RouterLink>

        <RouterLink
          to="/work"
          class="rounded-lg px-3 py-3 text-sm font-medium text-[#111827] transition hover:bg-[#F8F9FB] hover:text-[#635BFF]"
          active-class="bg-[#F8F9FB] !text-[#635BFF]"
          @click="closeMenu"
        >
          Work
        </RouterLink>

        <RouterLink
          to="/about"
          class="rounded-lg px-3 py-3 text-sm font-medium text-[#111827] transition hover:bg-[#F8F9FB] hover:text-[#635BFF]"
          active-class="bg-[#F8F9FB] !text-[#635BFF]"
          @click="closeMenu"
        >
          About
        </RouterLink>

        <RouterLink
          to="/contact"
          class="mt-2 rounded-lg bg-[#111827] px-5 py-3 text-center text-sm font-semibold text-white transition hover:bg-[#635BFF]"
          @click="closeMenu"
        >
          Start a Project
        </RouterLink>

      </div>
    </div>
  </header>
</template>