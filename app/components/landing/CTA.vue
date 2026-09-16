<template>
  <section
    id="contact"
    ref="section"
    class="relative isolate overflow-hidden bg-[#050706] py-32 sm:py-40 lg:py-52"
  >
    <!-- Ambient Emerald Glow -->
    <div
      class="pointer-events-none absolute left-1/2 top-1/2 -z-10 size-[650px] -translate-x-1/2 -translate-y-1/2 rounded-full bg-emerald-400/[0.09] blur-[160px]"
    ></div>

    <!-- Decorative Grid -->
    <div
      class="pointer-events-none absolute inset-0 -z-10 bg-[linear-gradient(to_right,rgba(255,255,255,0.025)_1px,transparent_1px),linear-gradient(to_bottom,rgba(255,255,255,0.025)_1px,transparent_1px)] bg-[size:64px_64px]"
    ></div>

    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div
        class="relative overflow-hidden rounded-3xl border border-white/[0.08] bg-white/[0.025] px-6 py-20 text-center sm:px-10 sm:py-28 lg:py-32"
      >
        <!-- Inner Glow -->
        <div
          class="pointer-events-none absolute left-1/2 top-0 h-px w-1/2 -translate-x-1/2 bg-gradient-to-r from-transparent via-emerald-400/50 to-transparent"
        ></div>

        <!-- Kicker -->
        <p
          ref="eyebrow"
          class="text-xs font-medium uppercase tracking-[0.3em] text-emerald-400"
        >
          Ready when you are
        </p>

        <!-- Heading -->
        <h2
          ref="heading"
          class="mx-auto mt-6 max-w-4xl text-5xl font-semibold leading-[0.95] tracking-[-0.05em] text-white sm:text-7xl lg:text-8xl"
        >
          Let's create
          <span class="block text-white/30">something remarkable.</span>
        </h2>

        <!-- Description -->
        <p
          ref="description"
          class="mx-auto mt-8 max-w-xl text-sm leading-7 text-white/40 sm:text-base"
        >
          Have an idea worth bringing to life? Let's turn it into an experience
          people remember.
        </p>

        <!-- CTA -->
        <div class="mt-10">
          <NuxtLink
            ref="action"
            href="mailto:hello@example.com"
            class="group inline-flex h-13 items-center gap-3 rounded-xl bg-emerald-400 px-7 p-4 text-sm font-semibold text-black shadow-2xl shadow-emerald-400/10 transition-all hover:bg-emerald-300 hover:shadow-emerald-400/20"
          >
            Start a conversation

            <span
              class="flex size-6 items-center justify-center rounded-full bg-black/10"
            >
              <svg
                class="size-3.5 transition-transform group-hover:translate-x-0.5"
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
            </span>
          </NuxtLink>
        </div>

        <!-- Bottom Label -->
        <div
          class="mx-auto mt-16 flex max-w-md items-center justify-center gap-4"
        >
          <span class="h-px flex-1 bg-white/[0.08]"></span>

          <span
            class="text-[10px] font-medium uppercase tracking-[0.2em] text-white/25"
          >
            Make it happen
          </span>

          <span class="h-px flex-1 bg-white/[0.08]"></span>
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
const action = ref<HTMLElement | null>(null);

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
          y: 20,
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
      );
  }, section.value);

  onUnmounted(() => {
    ctx.revert();
  });
});
</script>