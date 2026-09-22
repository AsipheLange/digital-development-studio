<script setup>
import { ref } from 'vue'

const form = ref({
  name: '',
  email: '',
  business: '',
  phone: '',
  projectType: '',
  description: '',
  budget: '',
  timeframe: '',
})

const submitted = ref(false)

const submitForm = () => {
  submitted.value = true
}
</script>

<template>
  <main>

    <!-- Contact Hero -->
    <section class="bg-[#F8F9FB] py-20 lg:py-28">
      <div class="mx-auto max-w-4xl px-6 text-center lg:px-8">

        <p
          class="mb-3 text-sm font-semibold uppercase tracking-wider text-[#635BFF]"
        >
          Start a project
        </p>

        <h1
          class="text-4xl font-bold tracking-tight text-[#111827] sm:text-5xl lg:text-6xl"
        >
          Let's build something useful.
        </h1>

        <p
          class="mx-auto mt-6 max-w-2xl text-lg leading-8 text-[#6B7280]"
        >
          Tell us a little about your business and what you'd like
          to build. We'll use your information to understand the
          project and determine the next steps.
        </p>

      </div>
    </section>

    <!-- Contact Form -->
    <section class="bg-white py-20 lg:py-28">
      <div class="mx-auto max-w-3xl px-6 lg:px-8">

        <div
          v-if="submitted"
          class="rounded-2xl border border-[#E5E7EB] bg-[#F8F9FB] p-10 text-center"
        >
          <div
            class="mx-auto flex h-14 w-14 items-center justify-center rounded-full bg-[#14B8A6]/10 text-2xl"
          >
            ✓
          </div>

          <h2 class="mt-6 text-2xl font-bold text-[#111827]">
            Thanks for reaching out!
          </h2>

          <p class="mx-auto mt-3 max-w-lg leading-7 text-[#6B7280]">
            Your project enquiry has been received. We'll review
            the details and get back to you.
          </p>
        </div>

        <form
          v-else
          class="space-y-8"
          @submit.prevent="submitForm"
        >

          <!-- Contact Details -->
          <div>
            <h2 class="text-xl font-bold text-[#111827]">
              Your details
            </h2>

            <p class="mt-1 text-sm text-[#6B7280]">
              Tell us how we can reach you.
            </p>

            <div class="mt-6 grid gap-6 sm:grid-cols-2">

              <!-- Name -->
              <div>
                <label
                  for="name"
                  class="block text-sm font-medium text-[#111827]"
                >
                  Name
                </label>

                <input
                  id="name"
                  v-model="form.name"
                  type="text"
                  required
                  placeholder="Your name"
                  class="mt-2 w-full rounded-xl border border-[#E5E7EB] bg-white px-4 py-3 text-sm outline-none transition placeholder:text-[#9CA3AF] focus:border-[#635BFF] focus:ring-2 focus:ring-[#635BFF]/10"
                />
              </div>

              <!-- Email -->
              <div>
                <label
                  for="email"
                  class="block text-sm font-medium text-[#111827]"
                >
                  Email
                </label>

                <input
                  id="email"
                  v-model="form.email"
                  type="email"
                  required
                  placeholder="you@example.com"
                  class="mt-2 w-full rounded-xl border border-[#E5E7EB] bg-white px-4 py-3 text-sm outline-none transition placeholder:text-[#9CA3AF] focus:border-[#635BFF] focus:ring-2 focus:ring-[#635BFF]/10"
                />
              </div>

              <!-- Business -->
              <div>
                <label
                  for="business"
                  class="block text-sm font-medium text-[#111827]"
                >
                  Business name
                </label>

                <input
                  id="business"
                  v-model="form.business"
                  type="text"
                  placeholder="Your business"
                  class="mt-2 w-full rounded-xl border border-[#E5E7EB] bg-white px-4 py-3 text-sm outline-none transition placeholder:text-[#9CA3AF] focus:border-[#635BFF] focus:ring-2 focus:ring-[#635BFF]/10"
                />
              </div>

              <!-- Phone -->
              <div>
                <label
                  for="phone"
                  class="block text-sm font-medium text-[#111827]"
                >
                  Phone
                </label>

                <input
                  id="phone"
                  v-model="form.phone"
                  type="tel"
                  placeholder="Your phone number"
                  class="mt-2 w-full rounded-xl border border-[#E5E7EB] bg-white px-4 py-3 text-sm outline-none transition placeholder:text-[#9CA3AF] focus:border-[#635BFF] focus:ring-2 focus:ring-[#635BFF]/10"
                />
              </div>

            </div>
          </div>

          <!-- Project Details -->
          <div>
            <h2 class="text-xl font-bold text-[#111827]">
              Your project
            </h2>

            <p class="mt-1 text-sm text-[#6B7280]">
              Give us a little more information about what you need.
            </p>

            <div class="mt-6 space-y-6">

              <!-- Project Type -->
              <div>
                <label
                  for="projectType"
                  class="block text-sm font-medium text-[#111827]"
                >
                  What would you like to build?
                </label>

                <select
                  id="projectType"
                  v-model="form.projectType"
                  required
                  class="mt-2 w-full rounded-xl border border-[#E5E7EB] bg-white px-4 py-3 text-sm text-[#111827] outline-none transition focus:border-[#635BFF] focus:ring-2 focus:ring-[#635BFF]/10"
                >
                  <option value="" disabled>
                    Select a project type
                  </option>

                  <option value="website">
                    Website
                  </option>

                  <option value="web-application">
                    Web Application
                  </option>

                  <option value="ecommerce">
                    E-Commerce
                  </option>

                  <option value="business-system">
                    Business System
                  </option>

                  <option value="other">
                    Something else
                  </option>
                </select>
              </div>

              <!-- Description -->
              <div>
                <label
                  for="description"
                  class="block text-sm font-medium text-[#111827]"
                >
                  Tell us about the project
                </label>

                <textarea
                  id="description"
                  v-model="form.description"
                  rows="6"
                  required
                  placeholder="What are you trying to build or improve?"
                  class="mt-2 w-full resize-none rounded-xl border border-[#E5E7EB] bg-white px-4 py-3 text-sm outline-none transition placeholder:text-[#9CA3AF] focus:border-[#635BFF] focus:ring-2 focus:ring-[#635BFF]/10"
                ></textarea>
              </div>

              <!-- Budget -->
              <div>
                <label
                  for="budget"
                  class="block text-sm font-medium text-[#111827]"
                >
                  Estimated budget
                </label>

                <select
                  id="budget"
                  v-model="form.budget"
                  class="mt-2 w-full rounded-xl border border-[#E5E7EB] bg-white px-4 py-3 text-sm text-[#111827] outline-none transition focus:border-[#635BFF] focus:ring-2 focus:ring-[#635BFF]/10"
                >
                  <option value="" disabled>
                    Select a budget range
                  </option>

                  <option value="under-5000">
                    Under R5,000
                  </option>

                  <option value="5000-10000">
                    R5,000 – R10,000
                  </option>

                  <option value="10000-20000">
                    R10,000 – R20,000
                  </option>

                  <option value="20000-plus">
                    R20,000+
                  </option>

                  <option value="not-sure">
                    I'm not sure yet
                  </option>
                </select>
              </div>

              <!-- Timeframe -->
              <div>
                <label
                  for="timeframe"
                  class="block text-sm font-medium text-[#111827]"
                >
                  Desired timeframe
                </label>

                <select
                  id="timeframe"
                  v-model="form.timeframe"
                  class="mt-2 w-full rounded-xl border border-[#E5E7EB] bg-white px-4 py-3 text-sm text-[#111827] outline-none transition focus:border-[#635BFF] focus:ring-2 focus:ring-[#635BFF]/10"
                >
                  <option value="" disabled>
                    Select a timeframe
                  </option>

                  <option value="asap">
                    As soon as possible
                  </option>

                  <option value="1-month">
                    Within 1 month
                  </option>

                  <option value="1-3-months">
                    1–3 months
                  </option>

                  <option value="3-plus-months">
                    3+ months
                  </option>

                  <option value="flexible">
                    I'm flexible
                  </option>
                </select>
              </div>

            </div>
          </div>

          <!-- Submit -->
          <div class="border-t border-[#E5E7EB] pt-8">

            <button
              type="submit"
              class="inline-flex w-full items-center justify-center rounded-xl bg-[#111827] px-6 py-3.5 font-semibold text-white transition hover:bg-[#635BFF] sm:w-auto"
            >
              Send Project Enquiry
              <span class="ml-2">→</span>
            </button>

            <p class="mt-3 text-xs text-[#9CA3AF]">
              This form is currently a demo and does not send data
              anywhere yet.
            </p>

          </div>

        </form>

      </div>
    </section>

  </main>
</template>