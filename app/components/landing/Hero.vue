<template>
  <section
    id="home"
    class="relative isolate flex min-h-screen items-center overflow-hidden bg-[#050706] pt-28"
  >
    <!-- Background Grid -->
    <div
      class="pointer-events-none absolute inset-0 -z-10 bg-[linear-gradient(to_right,rgba(255,255,255,0.035)_1px,transparent_1px),linear-gradient(to_bottom,rgba(255,255,255,0.035)_1px,transparent_1px)] bg-[size:64px_64px]"
    ></div>

    <!-- Emerald Ambient Glow -->
    <div
      class="pointer-events-none absolute left-1/2 top-1/2 -z-10 size-[600px] -translate-x-1/2 -translate-y-1/2 rounded-full bg-emerald-400/[0.08] blur-[140px]"
    ></div>

    <!-- Top Glow -->
    <div
      class="pointer-events-none absolute left-1/2 top-0 -z-10 h-[300px] w-[700px] -translate-x-1/2 rounded-full bg-emerald-400/[0.05] blur-[120px]"
    ></div>

    <div class="mx-auto w-full max-w-7xl px-6 py-24 lg:px-8">
      <div class="mx-auto max-w-5xl text-center">
        <!-- Eyebrow -->
        <div
          ref="eyebrow"
          class="mb-8 inline-flex items-center gap-2 rounded-full border border-emerald-400/20 bg-emerald-400/[0.05] px-3 py-1.5"
        >
          <span class="size-1.5 rounded-full bg-emerald-400"></span>

          <span
            class="text-xs font-medium uppercase tracking-[0.2em] text-emerald-300"
          >
            The future starts here
          </span>
        </div>

        <!-- Heading -->
        <h1
          ref="heading"
          class="text-balance text-5xl font-semibold leading-[0.95] tracking-[-0.04em] text-white sm:text-7xl md:text-8xl lg:text-[7rem]"
        >
          Build something
          <span class="block text-emerald-400"> unforgettable. </span>
        </h1>

        <!-- Description -->
        <p
          ref="description"
          class="mx-auto mt-8 max-w-2xl text-pretty text-base leading-7 text-white/50 sm:text-lg"
        >
          A modern digital experience built for people who care about beautiful
          interfaces, thoughtful interactions, and exceptional products.
        </p>

        <!-- Actions -->
        <div
          ref="actions"
          class="mt-10 flex flex-col items-center justify-center gap-3 sm:flex-row"
        >
          <a
            href="#features"
            class="group inline-flex h-12 items-center gap-2 rounded-xl bg-emerald-400 px-6 text-sm font-semibold text-black shadow-xl shadow-emerald-400/10 transition-all hover:bg-emerald-300 hover:shadow-emerald-400/20"
          >
            Explore the experience

            <svg
              class="size-4 transition-transform group-hover:translate-x-0.5"
              viewBox="0 0 16 16"
              fill="none"
              aria-hidden="true"
            >
              <path
                d="M3.5 8h9M8.5 4.5 12 8l-3.5 3.5"
                stroke="currentColor"
                stroke-width="1.5"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </a>

          <a
            href="#about"
            class="inline-flex h-12 items-center rounded-xl border border-white/10 bg-white/[0.03] px-6 text-sm font-medium text-white/80 backdrop-blur-sm transition-colors hover:bg-white/[0.06] hover:text-white"
          >
            Learn more
          </a>
        </div>
      </div>

      <!-- Bottom Meta -->
      <div
        class="mt-24 flex items-center justify-between border-t border-white/[0.08] pt-5"
      >
        <div class="flex items-center gap-3">
          <span class="size-1.5 rounded-full bg-emerald-400"></span>

          <span
            class="text-[10px] font-medium uppercase tracking-[0.2em] text-white/30"
          >
            Available worldwide
          </span>
        </div>

        <div
          class="hidden text-[10px] font-medium uppercase tracking-[0.2em] text-white/30 sm:block"
        >
          Scroll to explore
        </div>

        <div
          class="text-[10px] font-medium uppercase tracking-[0.2em] text-white/30"
        >
          2026
        </div>
      </div>
    </div>

    <!-- Decorative Side Lines -->
    <div
      class="pointer-events-none absolute left-6 top-1/2 hidden h-32 w-px -translate-y-1/2 bg-gradient-to-b from-transparent via-emerald-400/30 to-transparent lg:block"
    ></div>

    <div
      class="pointer-events-none absolute right-6 top-1/2 hidden h-32 w-px -translate-y-1/2 bg-gradient-to-b from-transparent via-emerald-400/30 to-transparent lg:block"
    ></div>
  </section>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue';

const { $gsap } = useNuxtApp();

const eyebrow = ref<HTMLElement | null>(null);
const heading = ref<HTMLElement | null>(null);
const description = ref<HTMLElement | null>(null);
const actions = ref<HTMLElement | null>(null);

onMounted(() => {
  const timeline = $gsap.timeline();

  timeline
    .from(eyebrow.value, {
      opacity: 0,
      y: 20,
      duration: 0.6,
    })
    .from(
      heading.value,
      {
        opacity: 0,
        y: 40,
        duration: 0.8,
      },
      '-=0.3',
    )
    .from(
      description.value,
      {
        opacity: 0,
        y: 24,
        duration: 0.6,
      },
      '-=0.4',
    )
    .from(
      actions.value,
      {
        opacity: 0,
        y: 20,
        duration: 0.5,
      },
      '-=0.3',
    );
});
</script>
