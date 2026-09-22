<script setup>
import {
  Search,
  ClipboardList,
  Palette,
  Code2,
  Rocket,
} from '@lucide/vue'

const steps = [
  {
    number: '01',
    title: 'Discover',
    description:
      'We learn about your business, goals and the problem you want to solve.',
    icon: Search,
  },
  {
    number: '02',
    title: 'Plan',
    description:
      'We define the features, structure and approach needed to bring the project together.',
    icon: ClipboardList,
  },
  {
    number: '03',
    title: 'Design',
    description:
      'We create a clean, responsive experience designed around your users and your brand.',
    icon: Palette,
  },
  {
    number: '04',
    title: 'Build',
    description:
      'We develop, test and refine your website or application using modern technologies.',
    icon: Code2,
  },
  {
    number: '05',
    title: 'Launch',
    description:
      'Once everything is ready, we help get your digital solution live and ready for your customers.',
    icon: Rocket,
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
          How it works
        </p>

        <h2
          class="text-3xl font-bold tracking-tight text-[#111827] sm:text-4xl"
        >
          From idea to launch.
        </h2>

        <p class="mt-4 text-lg leading-8 text-[#6B7280]">
          A simple, collaborative process designed to turn your
          business needs into a practical digital solution.
        </p>
      </div>

      <!-- Steps -->
      <div class="relative mt-14">

        <!-- Connecting Line -->
        <div
          class="absolute left-[10%] right-[10%] top-7 hidden h-px bg-[#E5E7EB] md:block"
        ></div>

        <div class="grid gap-10 md:grid-cols-5">

          <div
            v-for="(step, index) in steps"
            :key="step.number"
            class="relative text-center"
          >

            <!-- Icon -->
            <div
             class="relative z-10 mx-auto flex h-14 w-14 items-center justify-center rounded-full border-4 border-white shadow-sm"
            :class="
               index === 0
                 ? 'bg-[#635BFF] text-white'
                 : index === steps.length - 1
                   ? 'bg-[#14B8A6] text-white'
                   : 'bg-[#F8F9FB] text-[#635BFF]'
             "
>
              <component
                :is="step.icon"
                :size="22"
                :stroke-width="1.8"
              />
            </div>

            <!-- Number -->
            <p
              class="mt-5 text-xs font-bold tracking-widest text-[#635BFF]"
            >
              {{ step.number }}
            </p>

            <!-- Title -->
            <h3 class="mt-2 font-bold text-[#111827]">
              {{ step.title }}
            </h3>

            <!-- Description -->
            <p class="mt-2 text-sm leading-6 text-[#6B7280]">
              {{ step.description }}
            </p>

          </div>

        </div>
      </div>

    </div>
  </section>
</template>