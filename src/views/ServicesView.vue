<template>
  <main>

    <!-- Hero -->
    <section class="bg-[#F8F9FB] py-20 lg:py-28">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="max-w-3xl">

          <p
            class="mb-4 text-sm font-semibold uppercase tracking-wider text-[#635BFF]"
          >
            Our services
          </p>

          <h1
            class="text-4xl font-bold tracking-tight text-[#111827] sm:text-5xl lg:text-6xl"
          >
            Digital solutions built around your business.
          </h1>

          <p
            class="mt-6 max-w-2xl text-lg leading-8 text-[#6B7280]"
          >
            From professional websites to custom business systems,
            we build practical digital solutions designed around
            your goals, customers and everyday operations.
          </p>

        </div>
      </div>
    </section>

    <!-- Services -->
    <section class="bg-white py-20 lg:py-28">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">

        <div class="grid gap-8 md:grid-cols-2">

          <!-- Websites -->
          <article
            class="rounded-2xl border border-[#E5E7EB] bg-white p-8 transition hover:-translate-y-1 hover:shadow-xl"
          >
            <div
              class="flex h-12 w-12 items-center justify-center rounded-xl bg-[#635BFF]/10 text-[#635BFF]"
            >
              <span class="text-xl">01</span>
            </div>

            <h2 class="mt-6 text-2xl font-bold text-[#111827]">
              Websites
            </h2>

            <p class="mt-4 leading-7 text-[#6B7280]">
              Modern, responsive websites that give your business
              a professional online presence and make it easy for
              customers to find and understand what you offer.
            </p>

            <ul class="mt-6 space-y-3 text-sm text-[#6B7280]">
              <li>✓ Business websites</li>
              <li>✓ Landing pages</li>
              <li>✓ Responsive design</li>
              <li>✓ Contact and enquiry forms</li>
              <li>✓ Deployment and setup</li>
            </ul>
          </article>

          <!-- Web Applications -->
          <article
            class="rounded-2xl border border-[#E5E7EB] bg-white p-8 transition hover:-translate-y-1 hover:shadow-xl"
          >
            <div
              class="flex h-12 w-12 items-center justify-center rounded-xl bg-[#635BFF]/10 text-[#635BFF]"
            >
              <span class="text-xl">02</span>
            </div>

            <h2 class="mt-6 text-2xl font-bold text-[#111827]">
              Web Applications
            </h2>

            <p class="mt-4 leading-7 text-[#6B7280]">
              Custom web applications built around specific business
              processes, customer experiences or operational needs.
            </p>

            <ul class="mt-6 space-y-3 text-sm text-[#6B7280]">
              <li>✓ Custom dashboards</li>
              <li>✓ User authentication</li>
              <li>✓ Database integration</li>
              <li>✓ REST API integration</li>
              <li>✓ Role-based functionality</li>
            </ul>
          </article>

          <!-- E-Commerce -->
          <article
            class="rounded-2xl border border-[#E5E7EB] bg-white p-8 transition hover:-translate-y-1 hover:shadow-xl"
          >
            <div
              class="flex h-12 w-12 items-center justify-center rounded-xl bg-[#14B8A6]/10 text-[#14B8A6]"
            >
              <span class="text-xl">03</span>
            </div>

            <h2 class="mt-6 text-2xl font-bold text-[#111827]">
              E-Commerce
            </h2>

            <p class="mt-4 leading-7 text-[#6B7280]">
              Online stores that help businesses showcase products,
              manage customers and create a simple purchasing experience.
            </p>

            <ul class="mt-6 space-y-3 text-sm text-[#6B7280]">
              <li>✓ Product catalogues</li>
              <li>✓ Shopping carts</li>
              <li>✓ Customer accounts</li>
              <li>✓ Order management</li>
              <li>✓ Payment integration</li>
            </ul>
          </article>

          <!-- Business Systems -->
          <article
            class="rounded-2xl border border-[#E5E7EB] bg-white p-8 transition hover:-translate-y-1 hover:shadow-xl"
          >
            <div
              class="flex h-12 w-12 items-center justify-center rounded-xl bg-[#14B8A6]/10 text-[#14B8A6]"
            >
              <span class="text-xl">04</span>
            </div>

            <h2 class="mt-6 text-2xl font-bold text-[#111827]">
              Business Systems & Automation
            </h2>

            <p class="mt-4 leading-7 text-[#6B7280]">
              Digital tools that help businesses reduce repetitive
              work, organise information and manage everyday operations.
            </p>

            <ul class="mt-6 space-y-3 text-sm text-[#6B7280]">
              <li>✓ Internal management systems</li>
              <li>✓ Data management</li>
              <li>✓ Workflow automation</li>
              <li>✓ Reporting dashboards</li>
              <li>✓ Business process tools</li>
            </ul>
          </article>

        </div>
      </div>
    </section>

    <!-- CTA -->
    <section class="bg-[#111827] py-20">
      <div class="mx-auto max-w-3xl px-6 text-center lg:px-8">

        <h2 class="text-3xl font-bold text-white sm:text-4xl">
          Not sure what you need?
        </h2>

        <p class="mt-5 text-lg leading-8 text-gray-300">
          Tell us about your business and what you're trying to
          achieve. We'll help you identify the right digital solution.
        </p>

        <RouterLink
          to="/contact"
          class="mt-8 inline-flex items-center rounded-xl bg-white px-6 py-3.5 font-semibold text-[#111827] transition hover:bg-[#635BFF] hover:text-white"
        >
          Start a Project
          <span class="ml-2">→</span>
        </RouterLink>

      </div>
    </section>

  </main>
</template>