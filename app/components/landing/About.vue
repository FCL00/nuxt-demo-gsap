<template>
  <section
    id="about"
    ref="section"
    class="relative overflow-hidden border-y border-white/[0.06] bg-[#050706] py-32 sm:py-40"
  >
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <!-- Eyebrow -->
      <p
        ref="eyebrow"
        class="mb-8 text-xs font-medium uppercase tracking-[0.25em] text-emerald-400"
      >
        Our approach
      </p>

      <!-- Main Statement -->
      <h2
        ref="heading"
        class="max-w-6xl text-balance text-4xl font-semibold leading-[1.05] tracking-[-0.04em] text-white sm:text-6xl lg:text-8xl"
      >
        We believe great digital experiences should feel
        <span class="text-white/30">simple, purposeful,</span>
        and
        <span class="text-emerald-400">alive.</span>
      </h2>

      <!-- Content -->
      <div class="mt-16 grid gap-10 lg:grid-cols-[1fr_0.7fr] lg:items-end">
        <p
          ref="description"
          class="max-w-2xl text-base leading-7 text-white/45 sm:text-lg"
        >
          We combine thoughtful design, modern technology, and meaningful
          interactions to create products that people enjoy using. No
          unnecessary complexity. No noise. Just experiences that work.
        </p>

        <div class="lg:justify-self-end">
          <a
            ref="action"
            href="#contact"
            class="group inline-flex items-center gap-2 text-sm font-semibold text-white transition-colors hover:text-emerald-400"
          >
            Let's build something

            <svg
              class="size-4 transition-transform group-hover:translate-x-1"
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
        </div>
      </div>

      <!-- Details -->
      <div
        ref="details"
        class="mt-24 grid border-t border-white/[0.08] pt-6 sm:grid-cols-3"
      >
        <div class="pb-6 sm:pb-0">
          <span
            class="text-[10px] font-medium uppercase tracking-[0.2em] text-white/25"
          >
            01
          </span>

          <p class="mt-3 text-sm text-white/50">Design with purpose</p>
        </div>

        <div class="border-white/[0.08] pb-6 sm:border-l sm:px-6 sm:pb-0">
          <span
            class="text-[10px] font-medium uppercase tracking-[0.2em] text-white/25"
          >
            02
          </span>

          <p class="mt-3 text-sm text-white/50">Built for people</p>
        </div>

        <div class="border-white/[0.08] sm:border-l sm:px-6">
          <span
            class="text-[10px] font-medium uppercase tracking-[0.2em] text-white/25"
          >
            03
          </span>

          <p class="mt-3 text-sm text-white/50">Made to last</p>
        </div>
      </div>
    </div>

    <!-- Ambient Glow -->
    <div
      class="pointer-events-none absolute -right-48 top-1/2 -z-10 size-[500px] -translate-y-1/2 rounded-full bg-emerald-400/[0.04] blur-[140px]"
    ></div>
  </section>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue';

const { $gsap } = useNuxtApp();

const section = ref<HTMLElement | null>(null);
const eyebrow = ref<HTMLElement | null>(null);
const heading = ref<HTMLElement | null>(null);
const description = ref<HTMLElement | null>(null);
const action = ref<HTMLElement | null>(null);
const details = ref<HTMLElement | null>(null);

onMounted(() => {
  if (!section.value) return;

  const ctx = $gsap.context(() => {
    const timeline = $gsap.timeline({
      scrollTrigger: {
        trigger: section.value,
        start: 'top 75%',
        once: true,
      },
    });

    timeline
      .from(eyebrow.value, {
        opacity: 0,
        y: 20,
        duration: 0.5,
        ease: 'power2.out',
      })
      .from(
        heading.value,
        {
          opacity: 0,
          y: 45,
          duration: 0.9,
          ease: 'power3.out',
        },
        '-=0.2',
      )
      .from(
        description.value,
        {
          opacity: 0,
          y: 25,
          duration: 0.6,
          ease: 'power2.out',
        },
        '-=0.4',
      )
      .from(
        action.value,
        {
          opacity: 0,
          y: 20,
          duration: 0.5,
          ease: 'power2.out',
        },
        '-=0.25',
      )
      .from(
        details.value,
        {
          opacity: 0,
          y: 15,
          duration: 0.5,
          ease: 'power2.out',
        },
        '-=0.25',
      );
  }, section.value);

  onUnmounted(() => {
    ctx.revert();
  });
});
</script>
