<script lang="ts">
  import { page } from '$app/state';
  import { resolve } from '$app/paths';

  type NavItem = {
    href: string;
    label: string;
  };

  const navItems: NavItem[] = [
    { href: '/', label: 'Home' },
    { href: '/about', label: 'About' },
    { href: '/contact', label: 'Contact' }
  ];

  let menuOpen = $state(false);

  const isActive = (href: string) => page.url.pathname === href;
</script>

<nav class="sticky top-0 z-50 border-b border-white/10 bg-slate-950/55 backdrop-blur-2xl supports-[backdrop-filter]:bg-slate-950/45">
  <div class="mx-auto max-w-7xl px-4 py-4 sm:px-6 lg:px-8">
    <div class="rounded-[1.5rem] border border-white/10 bg-white/5 px-4 py-3 shadow-[0_20px_50px_rgba(2,6,23,0.2)] backdrop-blur-xl sm:px-5">
      <div class="flex items-center justify-between gap-4">
        <a
          href={resolve('/')}
          class="group flex min-w-0 items-center gap-3.5"
          aria-label="Northstar Studio home"
          onclick={() => (menuOpen = false)}
        >
          <div class="flex h-14 w-14 shrink-0 items-center justify-center rounded-[1.25rem] bg-gradient-to-br from-sky-400 via-cyan-400 to-violet-500 text-lg font-bold tracking-tight text-slate-950 shadow-[0_18px_45px_rgba(96,165,250,0.25)] transition duration-300 group-hover:-translate-y-0.5 group-hover:scale-105">
            NS
          </div>
          <div class="min-w-0">
            <p class="truncate text-lg font-bold tracking-tight text-white sm:text-xl">Northstar Studio</p>
            <p class="truncate text-sm text-slate-400">Premium Digital Experiences</p>
          </div>
        </a>

        <div class="hidden items-center gap-2 lg:flex">
          {#each navItems as item (item.href)}
            <a
              href={resolve(item.href)}
              aria-current={isActive(item.href) ? 'page' : undefined}
              class={`group relative rounded-full px-4 py-2 text-sm font-medium transition duration-300 ${isActive(item.href) ? 'text-white' : 'text-slate-300 hover:text-white'}`}
              onclick={() => (menuOpen = false)}
            >
              {item.label}
              <span class={`absolute inset-x-3 -bottom-0.5 h-px rounded-full bg-gradient-to-r from-sky-400 to-violet-500 transition-all duration-300 ${isActive(item.href) ? 'opacity-100' : 'opacity-0 group-hover:opacity-70'}`}></span>
            </a>
          {/each}
        </div>

        <a
          href={resolve('/contact')}
          class="hidden rounded-full bg-gradient-to-r from-sky-400 to-violet-500 px-5 py-2.5 text-sm font-semibold text-white shadow-[0_18px_40px_rgba(96,165,250,0.24)] transition duration-300 hover:-translate-y-0.5 hover:shadow-[0_22px_50px_rgba(96,165,250,0.3)] lg:inline-flex"
          onclick={() => (menuOpen = false)}
        >
          Let&apos;s Talk
        </a>

        <button
          type="button"
          class="group inline-flex h-12 w-12 shrink-0 items-center justify-center rounded-full border border-white/10 bg-white/5 text-white transition duration-300 hover:border-sky-400/40 hover:bg-white/10 lg:hidden"
          aria-controls="mobile-menu"
          aria-expanded={menuOpen}
          aria-label="Toggle navigation menu"
          onclick={() => (menuOpen = !menuOpen)}
        >
          {#if menuOpen}
            <span class="text-2xl leading-none transition duration-300 group-hover:scale-110">×</span>
          {:else}
            <span class="flex flex-col gap-1.5 transition duration-300 group-hover:scale-105">
              <span class="block h-0.5 w-5 rounded-full bg-white transition"></span>
              <span class="block h-0.5 w-5 rounded-full bg-white transition"></span>
              <span class="block h-0.5 w-5 rounded-full bg-white transition"></span>
            </span>
          {/if}
        </button>
      </div>

      <div
        id="mobile-menu"
        class={`overflow-hidden transition-all duration-300 ease-out lg:hidden ${menuOpen ? 'max-h-96 pt-4 opacity-100' : 'max-h-0 opacity-0'}`}
      >
        <div class="space-y-2 border-t border-white/10 pt-4">
          {#each navItems as item (item.href)}
            <a
              href={resolve(item.href)}
              aria-current={isActive(item.href) ? 'page' : undefined}
              class={`block rounded-2xl px-4 py-3 text-sm font-medium transition duration-300 ${isActive(item.href) ? 'bg-sky-400/15 text-sky-200' : 'text-slate-300 hover:bg-white/5 hover:text-white'}`}
              onclick={() => (menuOpen = false)}
            >
              {item.label}
            </a>
          {/each}
          <a
            href={resolve('/contact')}
            class="block rounded-2xl bg-gradient-to-r from-sky-400 to-violet-500 px-4 py-3 text-center text-sm font-semibold text-white"
            onclick={() => (menuOpen = false)}
          >
            Let&apos;s Talk
          </a>
        </div>
      </div>
    </div>
  </div>
</nav>
