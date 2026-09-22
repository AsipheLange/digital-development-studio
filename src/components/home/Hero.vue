<template>
  <section class="relative overflow-hidden bg-[#F8F9FB]">
    <div
      class="mx-auto grid max-w-7xl items-center gap-16 px-6 py-20 lg:grid-cols-2 lg:px-8 lg:py-28"
    >

      <!-- Hero Content -->
      <div class="max-w-2xl">

        <!-- Eyebrow -->
        <div
          class="mb-6 inline-flex items-center gap-2 rounded-full border border-[#E5E7EB] bg-white px-4 py-2 text-sm font-medium text-[#6B7280]"
        >
          <span class="h-2 w-2 rounded-full bg-[#14B8A6]"></span>
          Digital Development Studio
        </div>

        <!-- Heading -->
        <h1
          class="text-5xl font-bold leading-tight tracking-tight text-[#111827] sm:text-6xl lg:text-7xl"
        >
          Digital solutions
          <span class="text-[#635BFF]">
            built around your business.
          </span>
        </h1>

        <!-- Description -->
        <p
          class="mt-6 max-w-xl text-lg leading-8 text-[#6B7280]"
        >
          We design and build modern websites and custom web applications
          that help businesses look professional, work smarter and serve
          their customers better.
        </p>

        <!-- Buttons -->
        <div class="mt-8 flex flex-col gap-4 sm:flex-row">

          <RouterLink
            to="/contact"
            class="inline-flex items-center justify-center rounded-xl bg-[#111827] px-6 py-3.5 font-semibold text-white transition hover:bg-[#635BFF]"
          >
            Start a Project
            <span class="ml-2">→</span>
          </RouterLink>

          <RouterLink
            to="/work"
            class="inline-flex items-center justify-center rounded-xl border border-[#E5E7EB] bg-white px-6 py-3.5 font-semibold text-[#111827] transition hover:border-[#635BFF] hover:text-[#635BFF]"
          >
            See My Work
          </RouterLink>

        </div>

        <!-- Small Trust Message -->
        <p class="mt-6 text-sm text-[#6B7280]">
          Built with modern technologies and a focus on real business needs.
        </p>

      </div>

      <!-- Hero Visual -->
      <div class="relative hidden lg:block">

        <!-- Decorative background -->
        <div
          class="absolute -right-10 -top-10 h-72 w-72 rounded-full bg-[#635BFF]/10 blur-3xl"
        ></div>

        <div
          class="absolute -bottom-10 -left-10 h-72 w-72 rounded-full bg-[#14B8A6]/10 blur-3xl"
        ></div>

        <!-- Browser Mockup -->
        <div
          class="relative rounded-2xl border border-[#E5E7EB] bg-white p-3 shadow-2xl"
        >

          <!-- Browser Bar -->
          <div
            class="flex items-center gap-2 border-b border-[#E5E7EB] px-3 pb-3"
          >
            <span class="h-3 w-3 rounded-full bg-[#E5E7EB]"></span>
            <span class="h-3 w-3 rounded-full bg-[#E5E7EB]"></span>
            <span class="h-3 w-3 rounded-full bg-[#E5E7EB]"></span>

            <div
              class="ml-4 h-7 flex-1 rounded-md bg-[#F8F9FB]"
            ></div>
          </div>

          <!-- Mock Website -->
          <div class="p-8">

            <div class="flex items-center justify-between">
              <div class="h-6 w-24 rounded bg-[#111827]"></div>

              <div class="flex gap-2">
                <div class="h-3 w-12 rounded bg-[#E5E7EB]"></div>
                <div class="h-3 w-12 rounded bg-[#E5E7EB]"></div>
                <div class="h-3 w-12 rounded bg-[#E5E7EB]"></div>
              </div>
            </div>

            <div class="mt-12">
              <div class="h-8 w-3/4 rounded bg-[#111827]"></div>
              <div class="mt-3 h-8 w-1/2 rounded bg-[#635BFF]"></div>

              <div class="mt-6 space-y-2">
                <div class="h-3 w-full rounded bg-[#E5E7EB]"></div>
                <div class="h-3 w-5/6 rounded bg-[#E5E7EB]"></div>
                <div class="h-3 w-2/3 rounded bg-[#E5E7EB]"></div>
              </div>

              <div class="mt-8 h-10 w-32 rounded-lg bg-[#111827]"></div>
            </div>

            <div class="mt-12 grid grid-cols-3 gap-3">
              <div class="h-24 rounded-xl bg-[#F8F9FB]"></div>
              <div class="h-24 rounded-xl bg-[#F8F9FB]"></div>
              <div class="h-24 rounded-xl bg-[#F8F9FB]"></div>
            </div>

          </div>
        </div>

      </div>

    </div>
  </section>
</template>