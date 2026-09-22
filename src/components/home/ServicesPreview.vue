<script setup>
import {
  Globe,
  LayoutDashboard,
  ShoppingCart,
  Workflow,
} from '@lucide/vue'

const services = [
  {
    title: 'Websites',
    description:
      'Modern, responsive websites that give your business a professional online presence.',
    icon: 'Globe',
  },
  {
    title: 'Web Applications',
    description:
      'Custom applications built to solve specific business problems and improve the way you work.',
    icon: 'LayoutDashboard',
  },
  {
    title: 'E-Commerce',
    description:
      'Online stores designed to help you showcase products, manage orders and serve customers.',
    icon: 'ShoppingCart',
  },
  {
    title: 'Business Systems & Automation',
    description:
      'Digital systems that streamline repetitive processes and make everyday operations easier.',
    icon: 'Workflow',
  },
]
</script>

<template>
  <section class="bg-[#F8F9FB] py-20 lg:py-28">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">

      <!-- Section Heading -->
      <div class="max-w-2xl">
        <p
          class="mb-3 text-sm font-semibold uppercase tracking-wider text-[#635BFF]"
        >
          What we build
        </p>

        <h2
          class="text-3xl font-bold tracking-tight text-[#111827] sm:text-4xl"
        >
          Digital solutions that work for you.
        </h2>

        <p class="mt-4 text-lg leading-8 text-[#6B7280]">
          From your first website to a custom business system, we build
          practical digital solutions around the way your business works.
        </p>
      </div>

      <!-- Services -->
      <div class="mt-12 grid gap-6 sm:grid-cols-2 lg:grid-cols-4">

        <div
          v-for="service in services"
          :key="service.title"
          class="group rounded-2xl border border-[#E5E7EB] bg-white p-6 transition duration-300 hover:-translate-y-1 hover:border-[#635BFF]/30 hover:shadow-xl"
        >

          <!-- Icon -->
          <div
            class="flex h-12 w-12 items-center justify-center rounded-xl bg-[#635BFF]/10 text-[#635BFF] transition group-hover:bg-[#635BFF] group-hover:text-white"
          >
            <Globe
              v-if="service.icon === 'Globe'"
              :size="24"
              :stroke-width="1.8"
            />

            <LayoutDashboard
              v-else-if="service.icon === 'LayoutDashboard'"
              :size="24"
              :stroke-width="1.8"
            />

            <ShoppingCart
              v-else-if="service.icon === 'ShoppingCart'"
              :size="24"
              :stroke-width="1.8"
            />

            <Workflow
              v-else-if="service.icon === 'Workflow'"
              :size="24"
              :stroke-width="1.8"
            />
          </div>

          <!-- Content -->
          <h3 class="mt-6 text-lg font-bold text-[#111827]">
            {{ service.title }}
          </h3>

          <p class="mt-3 text-sm leading-6 text-[#6B7280]">
            {{ service.description }}
          </p>

          <!-- Link -->
          <RouterLink
            to="/services"
            class="mt-5 inline-flex items-center text-sm font-semibold text-[#635BFF] transition group-hover:gap-2"
          >
            Learn more
            <span class="ml-1">→</span>
          </RouterLink>

        </div>

      </div>
    </div>
  </section>
</template>