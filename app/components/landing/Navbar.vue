<template>
  <header class="fixed inset-x-0 top-0 z-50 px-4 py-4 sm:px-6 lg:px-8">
    <nav
      class="mx-auto flex max-w-7xl items-center justify-between rounded-2xl border border-white/[0.08] bg-white/[0.035] px-4 py-3 shadow-2xl shadow-black/30 backdrop-blur-2xl backdrop-saturate-150 sm:px-5"
    >
      <!-- Logo -->
      <NuxtLink
        to="/"
        class="group flex items-center gap-2.5"
        aria-label="Home"
      >
        <span
          class="flex size-8 items-center justify-center rounded-lg bg-emerald-400 text-sm font-black text-black shadow-lg shadow-emerald-400/20"
        >
          B
        </span>

        <span class="text-sm font-semibold tracking-tight text-white">
          BUILDR<span class="text-emerald-400">.</span>
        </span>
      </NuxtLink>

      <!-- Desktop Navigation -->
      <div class="hidden items-center gap-1 md:flex">
        <a
          v-for="item in navigations"
          :key="item.href"
          :href="item.href"
          class="rounded-lg px-4 py-2 text-sm font-medium text-white/60 transition-colors hover:bg-white/[0.06] hover:text-white"
        >
          {{ item.label }}
        </a>
      </div>

      <!-- CTA -->
      <div class="hidden md:block">
        <a
          href="#contact"
          class="inline-flex items-center gap-2 rounded-lg border border-emerald-300/20 bg-emerald-400/90 px-4 py-2.5 text-sm font-semibold text-black shadow-lg shadow-emerald-400/10 transition-all hover:bg-emerald-300 hover:shadow-emerald-400/20"
        >
          Get started

          <svg
            class="size-4"
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

      <!-- Mobile Menu Button -->
      <button
        type="button"
        class="inline-flex size-9 items-center justify-center rounded-lg border border-white/[0.08] bg-white/[0.03] text-white/80 transition-colors hover:bg-white/[0.06] hover:text-white md:hidden"
        aria-label="Open navigation menu"
      >
        <svg class="size-5" viewBox="0 0 20 20" fill="none" aria-hidden="true">
          <path
            d="M3 6h14M3 10h14M3 14h14"
            stroke="currentColor"
            stroke-width="1.5"
            stroke-linecap="round"
          />
        </svg>
      </button>
    </nav>
  </header>
</template>

<script setup lang="ts">
const navigations = [
  {
    label: "Home",
    href: "#home",
  },
  {
    label: "Features",
    href: "#features",
  },
  {
    label: "About",
    href: "#about",
  },
  {
    label: "Contact",
    href: "#contact",
  },
];
</script>
