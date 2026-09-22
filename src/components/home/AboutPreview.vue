<script setup>
import {
  Target,
  Lightbulb,
  Code2,
  ArrowUpRight,
} from '@lucide/vue'

const principles = [
  {
    title: 'Business-focused',
    description: 'We start by understanding what your business actually needs.',
    icon: 'Target',
  },
  {
    title: 'Practical solutions',
    description: 'We focus on useful features that solve real problems.',
    icon: 'Lightbulb',
  },
  {
    title: 'Modern technology',
    description: 'We use reliable tools to build solutions that can grow with you.',
    icon: 'Code2',
  },
]
</script>

<template>
  <section class="bg-[#F8F9FB] py-20 lg:py-28">
    <div
      class="mx-auto grid max-w-7xl items-center gap-14 px-6 lg:grid-cols-2 lg:px-8"
    >

      <!-- Visual -->
      <div class="relative">

        <div
          class="absolute -left-6 -top-6 h-40 w-40 rounded-full bg-[#635BFF]/10 blur-3xl"
        ></div>

        <div
          class="absolute -bottom-6 -right-6 h-40 w-40 rounded-full bg-[#14B8A6]/10 blur-3xl"
        ></div>

        <div
          class="relative rounded-3xl border border-[#E5E7EB] bg-white p-6 shadow-xl"
        >

          <!-- Header -->
          <div class="flex items-center justify-between">

            <div class="flex items-center gap-3">

              <div
                class="flex h-11 w-11 items-center justify-center rounded-xl bg-[#635BFF] font-bold text-white"
              >
                DD
              </div>

              <div>
                <p class="text-sm font-bold text-[#111827]">
                  Digital Development
                </p>

                <p class="text-xs text-[#6B7280]">
                  Studio
                </p>
              </div>

            </div>

            <div
              class="rounded-full bg-[#14B8A6]/10 px-3 py-1 text-xs font-semibold text-[#14B8A6]"
            >
              Building
            </div>

          </div>

          <!-- Main Visual -->
          <div class="mt-8 rounded-2xl bg-[#111827] p-6">

            <div class="flex items-center gap-3">

              <div class="h-3 w-3 rounded-full bg-[#14B8A6]"></div>

              <p class="text-sm font-medium text-white">
                Digital solutions
              </p>

            </div>

            <div class="mt-8 space-y-3">
              <div class="h-4 w-3/4 rounded bg-white/20"></div>
              <div class="h-4 w-1/2 rounded bg-[#635BFF]"></div>
              <div class="h-3 w-2/3 rounded bg-white/10"></div>
            </div>

            <div class="mt-8 grid grid-cols-3 gap-3">
              <div class="h-20 rounded-xl bg-white/5"></div>
              <div class="h-20 rounded-xl bg-white/5"></div>
              <div class="h-20 rounded-xl bg-white/5"></div>
            </div>

          </div>

          <!-- Bottom -->
          <div class="mt-5 grid grid-cols-2 gap-4">

            <div class="rounded-xl bg-[#F8F9FB] p-4">

              <p class="text-xs text-[#6B7280]">
                Focus
              </p>

              <p class="mt-1 text-sm font-bold text-[#111827]">
                Your business
              </p>

            </div>

            <div class="rounded-xl bg-[#F8F9FB] p-4">

              <p class="text-xs text-[#6B7280]">
                Approach
              </p>

              <p class="mt-1 text-sm font-bold text-[#111827]">
                Purposeful
              </p>

            </div>

          </div>

        </div>
      </div>

      <!-- Content -->
      <div>

        <p
          class="mb-3 text-sm font-semibold uppercase tracking-wider text-[#635BFF]"
        >
          Why Digital Development Studio
        </p>

        <h2
          class="text-3xl font-bold tracking-tight text-[#111827] sm:text-4xl"
        >
          Technology with a purpose.
        </h2>

        <p class="mt-5 text-lg leading-8 text-[#6B7280]">
          We believe technology should make your business easier to run,
          easier to find and easier for your customers to use.
        </p>

        <p class="mt-4 leading-7 text-[#6B7280]">
          That's why we don't start with technology. We start by
          understanding your business, your customers and the problem
          you're trying to solve.
        </p>

        <!-- Principles -->
        <div class="mt-8 space-y-5">

          <div
            v-for="principle in principles"
            :key="principle.title"
            class="flex gap-4"
          >

            <!-- Icon -->
            <div
              class="flex h-10 w-10 shrink-0 items-center justify-center rounded-lg bg-[#635BFF]/10 text-[#635BFF]"
            >

              <Target
                v-if="principle.icon === 'Target'"
                :size="20"
                :stroke-width="1.8"
              />

              <Lightbulb
                v-else-if="principle.icon === 'Lightbulb'"
                :size="20"
                :stroke-width="1.8"
              />

              <Code2
                v-else-if="principle.icon === 'Code2'"
                :size="20"
                :stroke-width="1.8"
              />

            </div>

            <!-- Text -->
            <div>

              <h3 class="font-bold text-[#111827]">
                {{ principle.title }}
              </h3>

              <p class="mt-1 text-sm leading-6 text-[#6B7280]">
                {{ principle.description }}
              </p>

            </div>

          </div>

        </div>

        <!-- Link -->
        <RouterLink
          to="/about"
          class="mt-8 inline-flex items-center font-semibold text-[#635BFF] transition hover:text-[#111827]"
        >
          Learn more about us
          <ArrowUpRight class="ml-1" :size="18" />
        </RouterLink>

      </div>

    </div>
  </section>
</template>