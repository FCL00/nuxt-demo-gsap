<template>
  <footer class="border-t border-white/[0.08] bg-[#050706]">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <!-- Main Footer -->
      <div class="grid gap-16 py-16 sm:py-20 md:grid-cols-[1.4fr_1fr_1fr_1fr]">
        <!-- Brand -->
        <div>
          <NuxtLink
            to="/"
            class="inline-flex items-center gap-2.5"
            aria-label="Home"
          >
            <span
              class="flex size-9 items-center justify-center rounded-lg bg-emerald-400 text-sm font-black text-black"
            >
              N
            </span>

            <span class="text-sm font-semibold tracking-tight text-white">
              BUILDR<span class="text-emerald-400">.</span>
            </span>
          </NuxtLink>

          <p class="mt-6 max-w-xs text-sm leading-6 text-white/35">
            Building thoughtful digital experiences with technology, creativity,
            and purpose.
          </p>

          <div class="mt-8 flex items-center gap-2">
            <span class="size-1.5 rounded-full bg-emerald-400" />

            <span
              class="text-[10px] font-medium uppercase tracking-[0.2em] text-white/25"
            >
              Available worldwide
            </span>
          </div>
        </div>

        <!-- Explore -->
        <div>
          <p
            class="text-[10px] font-medium uppercase tracking-[0.2em] text-white/25"
          >
            Explore
          </p>

          <nav class="mt-5 flex flex-col items-start gap-3">
            <a
              href="#home"
              class="text-sm text-white/50 transition-colors hover:text-white"
            >
              Home
            </a>

            <a
              href="#features"
              class="text-sm text-white/50 transition-colors hover:text-white"
            >
              Features
            </a>

            <a
              href="#showcase"
              class="text-sm text-white/50 transition-colors hover:text-white"
            >
              Showcase
            </a>

            <a
              href="#about"
              class="text-sm text-white/50 transition-colors hover:text-white"
            >
              About
            </a>
          </nav>
        </div>

        <!-- Connect -->
        <div>
          <p
            class="text-[10px] font-medium uppercase tracking-[0.2em] text-white/25"
          >
            Connect
          </p>

          <nav class="mt-5 flex flex-col items-start gap-3">
            <a
              href="#contact"
              class="text-sm text-white/50 transition-colors hover:text-white"
            >
              Contact
            </a>

            <a
              href="#"
              class="text-sm text-white/50 transition-colors hover:text-white"
            >
              Instagram
            </a>

            <a
              href="#"
              class="text-sm text-white/50 transition-colors hover:text-white"
            >
              LinkedIn
            </a>

            <a
              href="#"
              class="text-sm text-white/50 transition-colors hover:text-white"
            >
              GitHub
            </a>
          </nav>
        </div>

        <!-- Contact -->
        <div>
          <p
            class="text-[10px] font-medium uppercase tracking-[0.2em] text-white/25"
          >
            Say hello
          </p>

          <a
            href="mailto:hello@example.com"
            class="group mt-5 inline-flex items-center gap-2 text-sm text-white/70 transition-colors hover:text-emerald-400"
          >
            hello@example.com

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
          </a>
        </div>
      </div>

      <!-- Footer Bottom -->
      <div
        class="flex flex-col gap-4 border-t border-white/[0.08] py-6 sm:flex-row sm:items-center sm:justify-between"
      >
        <p
          class="text-[10px] font-medium uppercase tracking-[0.15em] text-white/20"
        >
          © 2026 NEXT. All rights reserved.
        </p>

        <div class="flex items-center gap-6">
          <a
            href="#"
            class="text-[10px] font-medium uppercase tracking-[0.15em] text-white/20 transition-colors hover:text-white/50"
          >
            Privacy
          </a>

          <a
            href="#"
            class="text-[10px] font-medium uppercase tracking-[0.15em] text-white/20 transition-colors hover:text-white/50"
          >
            Terms
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>
