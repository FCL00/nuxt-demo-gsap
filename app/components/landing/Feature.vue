<template>
  <section
    id="features"
    ref="section"
    class="relative overflow-hidden bg-[#050706] py-32 sm:py-40"
  >
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <!-- Section Header -->
      <div
        class="grid gap-8 border-b border-white/[0.08] pb-16 lg:grid-cols-[1fr_0.8fr] lg:items-end"
      >
        <div>
          <p
            ref="eyebrow"
            class="mb-5 text-xs font-medium uppercase tracking-[0.25em] text-emerald-400"
          >
            What makes it different
          </p>

          <h2
            ref="heading"
            class="max-w-3xl text-4xl font-semibold leading-[0.95] tracking-[-0.04em] text-white sm:text-6xl lg:text-7xl"
          >
            Built with
            <span class="text-white/30">intention.</span>
          </h2>
        </div>

        <p
          ref="description"
          class="max-w-md text-base leading-7 text-white/45 lg:justify-self-end"
        >
          Every detail has a purpose. From the interface to the smallest
          interaction, everything is designed to create a better experience.
        </p>
      </div>

      <!-- Feature Grid -->
      <div class="grid gap-4 pt-4 md:grid-cols-2">
        <!-- Feature 01 -->
        <article
          ref="cards"
          class="group relative min-h-[360px] overflow-hidden rounded-2xl border border-white/[0.08] bg-white/[0.025] p-8 transition-colors hover:bg-white/[0.04] sm:p-10"
        >
          <!-- Glow -->
          <div
            class="pointer-events-none absolute -right-24 -top-24 size-64 rounded-full bg-emerald-400/[0.08] blur-[80px]"
          ></div>

          <div class="relative flex h-full flex-col justify-between">
            <div class="flex items-center justify-between">
              <span
                class="text-xs font-medium tracking-widest text-emerald-400"
              >
                01
              </span>

              <span
                class="flex size-10 items-center justify-center rounded-full border border-white/10 text-white/40"
              >
                <svg
                  class="size-4"
                  viewBox="0 0 16 16"
                  fill="none"
                  aria-hidden="true"
                >
                  <path
                    d="M4 12 12 4M5 4h7v7"
                    stroke="currentColor"
                    stroke-width="1.5"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                </svg>
              </span>
            </div>

            <div>
              <h3
                class="text-3xl font-semibold tracking-[-0.03em] text-white sm:text-4xl"
              >
                Thoughtful
                <span class="text-white/35">design.</span>
              </h3>

              <p class="mt-4 max-w-md text-sm leading-6 text-white/40">
                Clean interfaces, deliberate spacing, and a visual language
                designed to feel effortless.
              </p>
            </div>
          </div>
        </article>

        <!-- Feature 02 -->
        <article
          ref="cards"
          class="group relative min-h-[360px] overflow-hidden rounded-2xl border border-white/[0.08] bg-white/[0.025] p-8 transition-colors hover:bg-white/[0.04] sm:p-10"
        >
          <div
            class="pointer-events-none absolute -bottom-24 -left-24 size-64 rounded-full bg-emerald-400/[0.06] blur-[80px]"
          ></div>

          <div class="relative flex h-full flex-col justify-between">
            <div class="flex items-center justify-between">
              <span
                class="text-xs font-medium tracking-widest text-emerald-400"
              >
                02
              </span>

              <span
                class="flex size-10 items-center justify-center rounded-full border border-white/10 text-white/40"
              >
                <svg
                  class="size-4"
                  viewBox="0 0 16 16"
                  fill="none"
                  aria-hidden="true"
                >
                  <path
                    d="M8 2v12M2 8h12"
                    stroke="currentColor"
                    stroke-width="1.5"
                    stroke-linecap="round"
                  />
                </svg>
              </span>
            </div>

            <div>
              <h3
                class="text-3xl font-semibold tracking-[-0.03em] text-white sm:text-4xl"
              >
                Fast &
                <span class="text-white/35">reliable.</span>
              </h3>

              <p class="mt-4 max-w-md text-sm leading-6 text-white/40">
                Built with modern technology and performance in mind, so the
                experience stays fast wherever you are.
              </p>
            </div>
          </div>
        </article>

        <!-- Feature 03 -->
        <article
          ref="cards"
          class="group relative min-h-[300px] overflow-hidden rounded-2xl border border-white/[0.08] bg-white/[0.025] p-8 md:col-span-2 sm:p-10"
        >
          <div
            class="pointer-events-none absolute right-0 top-1/2 size-80 -translate-y-1/2 rounded-full bg-emerald-400/[0.05] blur-[100px]"
          ></div>

          <div
            class="relative grid gap-10 md:grid-cols-[auto_1fr] md:items-end"
          >
            <div>
              <span
                class="text-xs font-medium tracking-widest text-emerald-400"
              >
                03
              </span>

              <h3
                class="mt-6 max-w-xl text-3xl font-semibold tracking-[-0.03em] text-white sm:text-5xl"
              >
                Built for
                <span class="text-white/35">what's next.</span>
              </h3>
            </div>

            <div class="md:justify-self-end">
              <p class="max-w-md text-sm leading-6 text-white/40">
                Flexible foundations that grow with your ideas, your users, and
                whatever comes next.
              </p>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue';

const { $gsap } = useNuxtApp();

const section = ref<HTMLElement | null>(null);
const eyebrow = ref<HTMLElement | null>(null);
const heading = ref<HTMLElement | null>(null);
const description = ref<HTMLElement | null>(null);
const cards = ref<HTMLElement[]>([]);

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
          y: 30,
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
        cards.value,
        {
          opacity: 0,
          y: 50,
          duration: 0.7,
          stagger: 0.12,
          ease: 'power3.out',
        },
        '-=0.2',
      );
  }, section.value);

  onUnmounted(() => {
    ctx.revert();
  });
});
</script>
