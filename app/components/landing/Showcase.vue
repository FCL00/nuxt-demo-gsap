<template>
  <section
    id="showcase"
    ref="section"
    class="relative overflow-hidden border-t border-white/[0.06] bg-[#050706] py-32 sm:py-40"
  >
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <!-- Section Header -->
      <div class="mx-auto max-w-3xl text-center">
        <p
          ref="eyebrow"
          class="mb-5 text-xs font-medium uppercase tracking-[0.25em] text-emerald-400"
        >
          A closer look
        </p>

        <h2
          ref="heading"
          class="text-balance text-4xl font-semibold leading-[0.95] tracking-[-0.04em] text-white sm:text-6xl lg:text-7xl"
        >
          Designed to
          <span class="text-white/30">stand out.</span>
        </h2>

        <p
          ref="description"
          class="mx-auto mt-6 max-w-2xl text-base leading-7 text-white/45 sm:text-lg"
        >
          A visual system where thoughtful design and modern technology come
          together to create something distinctive.
        </p>
      </div>

      <!-- Showcase -->
      <div
        ref="showcase"
        class="relative mt-20 overflow-hidden rounded-3xl border border-white/[0.08] bg-white/[0.025] shadow-2xl shadow-black/40"
      >
        <!-- Browser Header -->
        <div
          class="flex h-12 items-center justify-between border-b border-white/[0.08] px-5"
        >
          <div class="flex items-center gap-1.5">
            <span class="size-2 rounded-full bg-white/15"></span>
            <span class="size-2 rounded-full bg-white/15"></span>
            <span class="size-2 rounded-full bg-white/15"></span>
          </div>

          <div
            class="hidden rounded-md border border-white/[0.06] bg-white/[0.025] px-16 py-1 text-[10px] text-white/20 sm:block"
          >
            next.example
          </div>

          <div class="size-4"></div>
        </div>

        <!-- Dashboard -->
        <div class="relative min-h-[420px] overflow-hidden bg-[#0a0d0b] p-5 sm:p-8">
          <!-- Ambient Glow -->
          <div
            class="pointer-events-none absolute left-1/2 top-1/2 size-[500px] -translate-x-1/2 -translate-y-1/2 rounded-full bg-emerald-400/[0.04] blur-[120px]"
          ></div>

          <div class="relative grid gap-4 lg:grid-cols-[220px_1fr]">
            <!-- Sidebar -->
            <div
              class="hidden rounded-2xl border border-white/[0.06] bg-white/[0.02] p-5 lg:block"
            >
              <div class="mb-8 flex items-center gap-2">
                <span
                  class="flex size-7 items-center justify-center rounded-lg bg-emerald-400 text-xs font-black text-black"
                >
                  N
                </span>

                <span class="text-xs font-semibold text-white/70">
                  NEXT.
                </span>
              </div>

              <div class="space-y-2">
                <div
                  class="h-8 rounded-lg bg-emerald-400/[0.08]"
                ></div>

                <div class="h-8 rounded-lg bg-white/[0.025]"></div>
                <div class="h-8 rounded-lg bg-white/[0.025]"></div>
                <div class="h-8 rounded-lg bg-white/[0.025]"></div>
              </div>
            </div>

            <!-- Main Dashboard -->
            <div class="space-y-4">
              <!-- Stats -->
              <div class="grid gap-4 sm:grid-cols-3">
                <div
                  class="rounded-2xl border border-white/[0.06] bg-white/[0.02] p-5"
                >
                  <div class="text-[10px] uppercase tracking-widest text-white/25">
                    Revenue
                  </div>

                  <div class="mt-3 text-2xl font-semibold text-white">
                    $48.2k
                  </div>

                  <div class="mt-2 text-xs text-emerald-400">
                    +18.4%
                  </div>
                </div>

                <div
                  class="rounded-2xl border border-white/[0.06] bg-white/[0.02] p-5"
                >
                  <div class="text-[10px] uppercase tracking-widest text-white/25">
                    Users
                  </div>

                  <div class="mt-3 text-2xl font-semibold text-white">
                    12.8k
                  </div>

                  <div class="mt-2 text-xs text-emerald-400">
                    +12.6%
                  </div>
                </div>

                <div
                  class="rounded-2xl border border-white/[0.06] bg-white/[0.02] p-5"
                >
                  <div class="text-[10px] uppercase tracking-widest text-white/25">
                    Growth
                  </div>

                  <div class="mt-3 text-2xl font-semibold text-white">
                    32.4%
                  </div>

                  <div class="mt-2 text-xs text-emerald-400">
                    +8.2%
                  </div>
                </div>
              </div>

              <!-- Chart -->
              <div
                class="relative min-h-[280px] overflow-hidden rounded-2xl border border-white/[0.06] bg-white/[0.02] p-5 sm:p-7"
              >
                <div class="flex items-center justify-between">
                  <div>
                    <div class="text-sm font-medium text-white/70">
                      Performance
                    </div>

                    <div class="mt-1 text-xs text-white/25">
                      Last 30 days
                    </div>
                  </div>

                  <div
                    class="rounded-lg border border-white/[0.06] px-3 py-1.5 text-[10px] text-white/30"
                  >
                    30 days
                  </div>
                </div>

                <!-- Chart -->
                <div class="absolute inset-x-7 bottom-7 top-24">
                  <svg
                    class="h-full w-full"
                    viewBox="0 0 800 240"
                    preserveAspectRatio="none"
                    fill="none"
                    aria-hidden="true"
                  >
                    <path
                      d="M0 205 C80 185 100 195 160 170 S250 145 310 155 S390 115 450 125 S520 75 585 95 S670 45 720 65 S770 25 800 35"
                      stroke="currentColor"
                      class="text-emerald-400"
                      stroke-width="3"
                    />

                    <path
                      d="M0 205 C80 185 100 195 160 170 S250 145 310 155 S390 115 450 125 S520 75 585 95 S670 45 720 65 S770 25 800 35 V240 H0 Z"
                      class="fill-emerald-400/[0.04]"
                    />
                  </svg>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Metadata -->
      <div
        ref="metadata"
        class="mt-6 grid gap-4 sm:grid-cols-3"
      >
        <div
          class="border-t border-white/[0.08] pt-4"
        >
          <span
            class="text-[10px] font-medium uppercase tracking-[0.2em] text-white/25"
          >
            Interface
          </span>

          <p class="mt-2 text-sm text-white/50">
            Clean by design
          </p>
        </div>

        <div
          class="border-t border-white/[0.08] pt-4"
        >
          <span
            class="text-[10px] font-medium uppercase tracking-[0.2em] text-white/25"
          >
            Technology
          </span>

          <p class="mt-2 text-sm text-white/50">
            Built for performance
          </p>
        </div>

        <div
          class="border-t border-white/[0.08] pt-4"
        >
          <span
            class="text-[10px] font-medium uppercase tracking-[0.2em] text-white/25"
          >
            Philosophy
          </span>

          <p class="mt-2 text-sm text-white/50">
            Less, but better
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue';

const { $gsap } = useNuxtApp();

const section = ref<HTMLElement | null>(null);
const eyebrow = ref<HTMLElement | null>(null);
const heading = ref<HTMLElement | null>(null);
const description = ref<HTMLElement | null>(null);
const showcase = ref<HTMLElement | null>(null);
const metadata = ref<HTMLElement | null>(null);

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
          y: 35,
          duration: 0.7,
          ease: 'power3.out',
        },
        '-=0.25',
      )
      .from(
        description.value,
        {
          opacity: 0,
          y: 20,
          duration: 0.5,
          ease: 'power2.out',
        },
        '-=0.35',
      )
      .from(
        showcase.value,
        {
          opacity: 0,
          y: 60,
          scale: 0.96,
          duration: 1,
          ease: 'power3.out',
        },
        '-=0.15',
      )
      .from(
        metadata.value,
        {
          opacity: 0,
          y: 15,
          duration: 0.5,
          ease: 'power2.out',
        },
        '-=0.4',
      );
  }, section.value);

  onUnmounted(() => {
    ctx.revert();
  });
});
</script>
