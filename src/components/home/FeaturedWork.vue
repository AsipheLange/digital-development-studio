<script setup>
import {
  ShoppingBag,
  UsersRound,
  ArrowUpRight,
} from '@lucide/vue'

const projects = [
  {
    title: 'Healthy Habits',
    category: 'E-Commerce / Web Application',
    description:
      'A prepared-meals e-commerce platform designed to help customers browse meals, manage their profiles and place orders online.',
    icon: 'ShoppingBag',
    technologies: ['Vue.js', 'Node.js', 'MySQL'],
  },
  {
    title: 'HR Management System',
    category: 'Business System / Web Application',
    description:
      'A business management system designed to simplify employee records, attendance, payroll and other everyday HR processes.',
    icon: 'UsersRound',
    technologies: ['JavaScript', 'SQL', 'REST API'],
  },
]
</script>

<template>
  <section class="bg-[#F8F9FB] py-20 lg:py-28">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">

      <!-- Heading -->
      <div class="flex flex-col gap-6 sm:flex-row sm:items-end sm:justify-between">

        <div class="max-w-2xl">
          <p
            class="mb-3 text-sm font-semibold uppercase tracking-wider text-[#635BFF]"
          >
            Featured work
          </p>

          <h2
            class="text-3xl font-bold tracking-tight text-[#111827] sm:text-4xl"
          >
            Projects built to solve real problems.
          </h2>

          <p class="mt-4 text-lg leading-8 text-[#6B7280]">
            A look at some of the websites, applications and systems
            we've built.
          </p>
        </div>

        <RouterLink
          to="/work"
          class="inline-flex shrink-0 items-center font-semibold text-[#635BFF] transition hover:text-[#111827]"
        >
          View all work
          <ArrowUpRight class="ml-1" :size="18" />
        </RouterLink>

      </div>

      <!-- Projects -->
      <div class="mt-12 grid gap-8 lg:grid-cols-2">

        <article
          v-for="project in projects"
          :key="project.title"
          class="group overflow-hidden rounded-2xl border border-[#E5E7EB] bg-white transition duration-300 hover:-translate-y-1 hover:shadow-xl"
        >

          <!-- Project Preview -->
          <div class="relative overflow-hidden bg-[#111827] p-4">

            <div
              class="rounded-xl border border-white/10 bg-white/5 p-3"
            >

              <!-- Browser Header -->
              <div class="flex items-center gap-2 border-b border-white/10 pb-3">
                <span class="h-2.5 w-2.5 rounded-full bg-white/20"></span>
                <span class="h-2.5 w-2.5 rounded-full bg-white/20"></span>
                <span class="h-2.5 w-2.5 rounded-full bg-white/20"></span>

                <div
                  class="ml-3 h-6 flex-1 rounded-md bg-white/10"
                ></div>
              </div>

              <!-- Mock Interface -->
              <div class="mt-4 rounded-lg bg-white p-5">

                <div class="flex items-center justify-between">

                  <div class="flex items-center gap-2">

                    <div
                      class="flex h-8 w-8 items-center justify-center rounded-lg bg-[#635BFF] text-white"
                    >
                      <ShoppingBag
                        v-if="project.icon === 'ShoppingBag'"
                        :size="16"
                      />

                      <UsersRound
                        v-else-if="project.icon === 'UsersRound'"
                        :size="16"
                      />
                    </div>

                    <div class="h-3 w-24 rounded bg-[#111827]"></div>

                  </div>

                  <div class="h-3 w-16 rounded bg-[#E5E7EB]"></div>

                </div>

                <div class="mt-7 grid grid-cols-3 gap-3">
                  <div class="h-20 rounded-lg bg-[#F8F9FB]"></div>
                  <div class="h-20 rounded-lg bg-[#F8F9FB]"></div>
                  <div class="h-20 rounded-lg bg-[#F8F9FB]"></div>
                </div>

                <div class="mt-4 space-y-2">
                  <div class="h-3 w-full rounded bg-[#E5E7EB]"></div>
                  <div class="h-3 w-4/5 rounded bg-[#E5E7EB]"></div>
                </div>

              </div>
            </div>
          </div>

          <!-- Project Details -->
          <div class="p-6">

            <p class="text-sm font-semibold text-[#635BFF]">
              {{ project.category }}
            </p>

            <h3 class="mt-2 text-2xl font-bold text-[#111827]">
              {{ project.title }}
            </h3>

            <p class="mt-3 leading-7 text-[#6B7280]">
              {{ project.description }}
            </p>

            <!-- Technologies -->
            <div class="mt-5 flex flex-wrap gap-2">

              <span
                v-for="technology in project.technologies"
                :key="technology"
                class="rounded-full border border-[#E5E7EB] bg-[#F8F9FB] px-3 py-1 text-xs font-medium text-[#6B7280]"
              >
                {{ technology }}
              </span>

            </div>

            <!-- Link -->
            <RouterLink
              to="/work"
              class="mt-6 inline-flex items-center text-sm font-semibold text-[#111827] transition group-hover:text-[#635BFF]"
            >
              View project
              <ArrowUpRight class="ml-1" :size="17" />
            </RouterLink>

          </div>

        </article>

      </div>
    </div>
  </section>
</template>