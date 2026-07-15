<script lang="ts">
  import { resolve } from '$app/paths';

  const footerLinks = [
    { href: '/', label: 'Home' },
    { href: '/about', label: 'About' },
    { href: '/contact', label: 'Contact' }
  ];

  const services = ['Web Development', 'UI/UX Design', 'Branding', 'Digital Marketing'];

  const socials = [
    {
      label: 'Facebook',
      href: 'https://facebook.com',
      icon: 'M24 8c-8.8 0-16 7.2-16 16 0 8 5.9 14.6 13.6 15.8V28.6h-4.1V24h4.1v-3.5c0-4 2.4-6.2 6-6.2 1.7 0 3.4.3 3.4.3v3.8h-1.9c-1.9 0-2.5 1.2-2.5 2.4V24H31l-.7 4.6h-4.8v11.2C33.1 38.6 40 31.9 40 24c0-8.8-7.2-16-16-16Z'
    },
    {
      label: 'LinkedIn',
      href: 'https://linkedin.com',
      icon: 'M11.4 10.8a2.6 2.6 0 1 1 0-5.2 2.6 2.6 0 0 1 0 5.2ZM8.6 35.2V14.8h5.6v20.4H8.6Zm9.3 0V14.8h5.4v2.8h.1c.8-1.5 2.7-3 5.4-3 5.7 0 6.8 3.8 6.8 8.8v11.8h-5.6V24.8c0-2.8 0-6.4-3.9-6.4-3.9 0-4.4 3.1-4.4 6.2v10.6h-5.8Z'
    },
    {
      label: 'Instagram',
      href: 'https://instagram.com',
      icon: 'M24 12.3c4.8 0 5.4 0 7.3.1 1.8.1 2.8.4 3.5.6.9.4 1.6.8 2.3 1.5.7.7 1.1 1.4 1.5 2.3.2.7.5 1.7.6 3.5.1 1.9.1 2.5.1 7.3s0 5.4-.1 7.3c-.1 1.8-.4 2.8-.6 3.5-.4.9-.8 1.6-1.5 2.3-.7.7-1.4 1.1-2.3 1.5-.7.2-1.7.5-3.5.6-1.9.1-2.5.1-7.3.1s-5.4 0-7.3-.1c-1.8-.1-2.8-.4-3.5-.6-.9-.4-1.6-.8-2.3-1.5-.7-.7-1.1-1.4-1.5-2.3-.2-.7-.5-1.7-.6-3.5-.1-1.9-.1-2.5-.1-7.3s0-5.4.1-7.3c.1-1.8.4-2.8.6-3.5.4-.9.8-1.6 1.5-2.3.7-.7 1.4-1.1 2.3-1.5.7-.2 1.7-.5 3.5-.6 1.9-.1 2.5-.1 7.3-.1Zm0 4.1c-4.7 0-5.2 0-7 .1-1.7.1-2.6.4-3.2.6-.8.3-1.4.7-2 1.3-.6.6-1 1.2-1.3 2-.2.6-.5 1.5-.6 3.2-.1 1.8-.1 2.3-.1 7s0 5.2.1 7c.1 1.7.4 2.6.6 3.2.3.8.7 1.4 1.3 2 .6.6 1.2 1 2 1.3.6.2 1.5.5 3.2.6 1.8.1 2.3.1 7 .1s5.2 0 7-.1c1.7-.1 2.6-.4 3.2-.6.8-.3 1.4-.7 2-1.3.6-.6 1-1.2 1.3-2 .2-.6.5-1.5.6-3.2.1-1.8.1-2.3.1-7s0-5.2-.1-7c-.1-1.7-.4-2.6-.6-3.2-.3-.8-.7-1.4-1.3-2-.6-.6-1.2-1-2-1.3-.6-.2-1.5-.5-3.2-.6-1.8-.1-2.3-.1-7-.1Zm0 18.4A6.4 6.4 0 1 1 24 17.5a6.4 6.4 0 0 1 0 12.8Zm0-10.6a4.2 4.2 0 1 0 0 8.4 4.2 4.2 0 0 0 0-8.4Zm7.7-4.7a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0Z'
    },
    {
      label: 'X',
      href: 'https://x.com',
      icon: 'M30.6 11.2h5.2l-11.4 13.1 13.4 17.5h-10.5l-8.2-10.7-9.3 10.7H4.6l12.2-14L4 11.2h10.7l7.4 9.8 8.5-9.8Zm-1.8 28.3h2.9L14.2 13.8h-3.1l17.7 25.7Z'
    }
  ];

  const year = new Date().getFullYear();

  const openSocial = (url: string) => {
    window.open(url, '_blank', 'noopener,noreferrer');
  };
</script>

<footer class="border-t border-white/10 bg-slate-950 text-white">
  <div class="mx-auto max-w-7xl px-4 py-16 sm:px-6 lg:px-8">
    <div class="grid gap-8 md:grid-cols-2 xl:grid-cols-4">
      <div class="rounded-[2rem] border border-white/10 bg-white/5 p-6 shadow-[0_24px_70px_rgba(2,6,23,0.24)] backdrop-blur-xl">
        <div class="flex items-center gap-3">
          <div class="flex h-12 w-12 items-center justify-center rounded-2xl bg-gradient-to-br from-sky-400 via-cyan-400 to-violet-500 text-base font-bold text-slate-950">
            NS
          </div>
          <div>
            <p class="text-lg font-bold tracking-tight text-white">Northstar Studio</p>
            <p class="text-sm text-slate-400">Premium digital experiences</p>
          </div>
        </div>
        <p class="mt-5 max-w-sm text-sm leading-7 text-slate-400">
          We design polished websites and brand experiences for companies that want to look modern, credible, and conversion-ready.
        </p>
        <div class="mt-6 flex items-center gap-3">
          {#each socials as social (social.label)}
            <button
              type="button"
              aria-label={social.label}
              onclick={() => openSocial(social.href)}
              class="group inline-flex h-11 w-11 items-center justify-center rounded-2xl border border-white/10 bg-white/5 text-slate-300 transition duration-300 hover:-translate-y-0.5 hover:border-sky-400/40 hover:bg-sky-400/10 hover:text-sky-200"
            >
              <svg viewBox="0 0 48 48" class="h-5 w-5 fill-current transition duration-300 group-hover:scale-110" aria-hidden="true">
                <path d={social.icon}></path>
              </svg>
            </button>
          {/each}
        </div>
      </div>

      <div>
        <p class="text-sm font-semibold uppercase tracking-[0.35em] text-slate-500">Quick Links</p>
        <div class="mt-5 flex flex-col gap-3">
          {#each footerLinks as item (item.href)}
            <a href={resolve(item.href)} class="text-sm text-slate-300 transition duration-300 hover:translate-x-1 hover:text-sky-200">
              {item.label}
            </a>
          {/each}
        </div>
      </div>

      <div>
        <p class="text-sm font-semibold uppercase tracking-[0.35em] text-slate-500">Services</p>
        <div class="mt-5 flex flex-col gap-3">
          {#each services as service (service)}
            <p class="text-sm text-slate-300 transition duration-300 hover:text-sky-200">{service}</p>
          {/each}
        </div>
      </div>

      <div>
        <p class="text-sm font-semibold uppercase tracking-[0.35em] text-slate-500">Contact</p>
        <div class="mt-5 space-y-3 text-sm text-slate-300">
          <p>hello@northstarstudio.lk</p>
          <p>+94 76 123 4567</p>
          <p>Colombo, Sri Lanka</p>
        </div>
      </div>
    </div>
  </div>

  <div class="border-t border-white/10 bg-white/[0.02]">
    <div class="mx-auto flex max-w-7xl flex-col gap-3 px-4 py-5 text-sm text-slate-500 sm:flex-row sm:items-center sm:justify-between sm:px-6 lg:px-8">
      <p>© {year} Northstar Studio. All Rights Reserved.</p>
      <p class="text-slate-400">Built for premium static delivery and a fast browsing experience.</p>
    </div>
  </div>
</footer>
