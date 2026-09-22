<template>
  <footer class="border-t border-[#E5E7EB] bg-white">
    <div class="mx-auto max-w-7xl px-6 py-14 lg:px-8">

      <div class="grid gap-10 md:grid-cols-2 lg:grid-cols-4">

        <!-- Brand -->
        <div class="lg:col-span-2">

          <RouterLink to="/" class="inline-flex items-center gap-3">
            <div
              class="flex h-10 w-10 items-center justify-center rounded-xl bg-[#635BFF] font-bold text-white"
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
          </RouterLink>

          <p class="mt-5 max-w-md leading-7 text-[#6B7280]">
            We design and build modern websites, web applications
            and digital solutions around your business.
          </p>

          <RouterLink
            to="/contact"
            class="mt-6 inline-flex items-center rounded-xl bg-[#111827] px-5 py-3 text-sm font-semibold text-white transition hover:bg-[#635BFF]"
          >
            Start a Project
            <span class="ml-2">→</span>
          </RouterLink>

        </div>

        <!-- Navigation -->
        <div>
          <h3 class="text-sm font-semibold text-[#111827]">
            Navigation
          </h3>

          <div class="mt-5 flex flex-col gap-3">

            <RouterLink
              to="/"
              class="text-sm text-[#6B7280] transition hover:text-[#635BFF]"
            >
              Home
            </RouterLink>

            <RouterLink
              to="/services"
              class="text-sm text-[#6B7280] transition hover:text-[#635BFF]"
            >
              Services
            </RouterLink>

            <RouterLink
              to="/work"
              class="text-sm text-[#6B7280] transition hover:text-[#635BFF]"
            >
              Work
            </RouterLink>

            <RouterLink
              to="/about"
              class="text-sm text-[#6B7280] transition hover:text-[#635BFF]"
            >
              About
            </RouterLink>

            <RouterLink
              to="/contact"
              class="text-sm text-[#6B7280] transition hover:text-[#635BFF]"
            >
              Contact
            </RouterLink>

          </div>
        </div>

        <!-- Services -->
        <div>
          <h3 class="text-sm font-semibold text-[#111827]">
            Services
          </h3>

          <div class="mt-5 flex flex-col gap-3">

            <RouterLink
              to="/services"
              class="text-sm text-[#6B7280] transition hover:text-[#635BFF]"
            >
              Websites
            </RouterLink>

            <RouterLink
              to="/services"
              class="text-sm text-[#6B7280] transition hover:text-[#635BFF]"
            >
              Web Applications
            </RouterLink>

            <RouterLink
              to="/services"
              class="text-sm text-[#6B7280] transition hover:text-[#635BFF]"
            >
              E-Commerce
            </RouterLink>

            <RouterLink
              to="/services"
              class="text-sm text-[#6B7280] transition hover:text-[#635BFF]"
            >
              Business Systems
            </RouterLink>

          </div>
        </div>

      </div>

      <!-- Bottom -->
      <div
        class="mt-12 flex flex-col gap-4 border-t border-[#E5E7EB] pt-6 text-sm text-[#6B7280] sm:flex-row sm:items-center sm:justify-between"
      >
        <p>
          © {{ new Date().getFullYear() }} Digital Development Studio.
          All rights reserved.
        </p>

        <p>
          Websites. Systems. Digital Solutions.
        </p>
      </div>

    </div>
  </footer>
</template>