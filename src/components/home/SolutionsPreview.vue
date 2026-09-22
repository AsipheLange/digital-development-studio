<script setup>
import {
  Building2,
  GraduationCap,
  Sparkles,
  UtensilsCrossed,
} from '@lucide/vue'

const solutions = [
  {
    title: 'Small Businesses',
    description:
      'Professional websites and digital tools that help your business grow and operate more efficiently.',
    icon: 'Building2',
  },
  {
    title: 'Education & Childcare',
    description:
      'Simple digital experiences for schools, creches and education-focused organisations.',
    icon: 'GraduationCap',
  },
  {
    title: 'Beauty & Wellness',
    description:
      'Digital solutions that help clients discover your services, book appointments and stay connected.',
    icon: 'Sparkles',
  },
  {
    title: 'Food & Hospitality',
    description:
      'Websites and online experiences that make it easier for customers to discover and engage with your business.',
    icon: 'UtensilsCrossed',
  },
]
</script>

<template>
  <section class="bg-white py-20 lg:py-28">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">

      <!-- Heading -->
      <div class="mx-auto max-w-2xl text-center">
        <p
          class="mb-3 text-sm font-semibold uppercase tracking-wider text-[#635BFF]"
        >
          Who we build for
        </p>

        <h2
          class="text-3xl font-bold tracking-tight text-[#111827] sm:text-4xl"
        >
          Built around your business.
        </h2>

        <p class="mt-4 text-lg leading-8 text-[#6B7280]">
          Every business is different. We create digital solutions
          that fit your goals, customers and day-to-day operations.
        </p>
      </div>

      <!-- Solutions -->
      <div class="mt-12 grid gap-6 sm:grid-cols-2 lg:grid-cols-4">

        <div
          v-for="solution in solutions"
          :key="solution.title"
          class="group rounded-2xl border border-[#E5E7EB] bg-[#F8F9FB] p-6 transition duration-300 hover:-translate-y-1 hover:border-[#635BFF]/30 hover:bg-white hover:shadow-xl"
        >

          <!-- Icon -->
          <div
            class="flex h-12 w-12 items-center justify-center rounded-xl bg-white text-[#635BFF] shadow-sm transition group-hover:bg-[#635BFF] group-hover:text-white"
          >
            <Building2
              v-if="solution.icon === 'Building2'"
              :size="24"
              :stroke-width="1.8"
            />

            <GraduationCap
              v-else-if="solution.icon === 'GraduationCap'"
              :size="24"
              :stroke-width="1.8"
            />

            <Sparkles
              v-else-if="solution.icon === 'Sparkles'"
              :size="24"
              :stroke-width="1.8"
            />

            <UtensilsCrossed
              v-else-if="solution.icon === 'UtensilsCrossed'"
              :size="24"
              :stroke-width="1.8"
            />
          </div>

          <!-- Content -->
          <h3 class="mt-6 text-lg font-bold text-[#111827]">
            {{ solution.title }}
          </h3>

          <p class="mt-3 text-sm leading-6 text-[#6B7280]">
            {{ solution.description }}
          </p>

        </div>

      </div>
    </div>
  </section>
</template>