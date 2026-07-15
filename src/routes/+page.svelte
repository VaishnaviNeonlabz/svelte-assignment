<script lang="ts">
  import { resolve } from '$app/paths';
  import ServiceCard from '$lib/components/ServiceCard.svelte';

  const trustedCompanies = ['Cloudbase', 'Kanba', 'Sitemark', 'Penta', 'Aven'];
  const stars = [0, 1, 2, 3, 4];

  const services = [
    {
      badge: '01',
      title: 'Web Development',
      description: 'Fast, reliable SvelteKit builds with clean structure, responsiveness, and launch-ready polish.',
      features: ['Custom builds', 'Responsive layouts', 'Performance focused'],
      accent: 'bg-gradient-to-br from-sky-500/15 via-cyan-500/10 to-blue-500/5',
      icon: 'M12 9h24c1.7 0 3 1.3 3 3v20c0 1.7-1.3 3-3 3H12c-1.7 0-3-1.3-3-3V12c0-1.7 1.3-3 3-3Zm0 6v17h24V15H12Zm4 4h7v3h-7v-3Zm0 6h16v3H16v-3Z'
    },
    {
      badge: '02',
      title: 'UI/UX Design',
      description: 'Elegant interfaces with strong hierarchy, thoughtful spacing, and conversion-friendly flow.',
      features: ['User flows', 'Interface systems', 'Design polish'],
      accent: 'bg-gradient-to-br from-violet-500/15 via-fuchsia-500/10 to-sky-500/5',
      icon: 'M24 8l14 6v10c0 8-5.2 13.5-14 17-8.8-3.5-14-9-14-17V14l14-6Zm0 6.2L14 18v6.8c0 5.3 3.5 9.2 10 12 6.5-2.8 10-6.7 10-12V18l-10-3.8Zm-1.5 6.8h3v4h4v3h-4v4h-3v-4h-4v-3h4v-4Z'
    },
    {
      badge: '03',
      title: 'Branding',
      description: 'Brand systems and visual language that make the company feel premium, memorable, and consistent.',
      features: ['Identity systems', 'Visual direction', 'Messaging clarity'],
      accent: 'bg-gradient-to-br from-cyan-500/15 via-teal-500/10 to-sky-500/5',
      icon: 'M20 9h16l6 6v16H20a4 4 0 0 1-4-4V13a4 4 0 0 1 4-4Zm2 4v16h20V17h-6v-6H22Zm8 2h6v6h-6v-6Z'
    },
    {
      badge: '04',
      title: 'Digital Marketing',
      description: 'Landing pages and campaign assets that support outreach, engagement, and measurable growth.',
      features: ['Campaign pages', 'Lead generation', 'Analytics ready'],
      accent: 'bg-gradient-to-br from-slate-500/15 via-indigo-500/10 to-violet-500/5',
      icon: 'M10 28c2.2 1.8 5.2 2.8 8 2.8 5.1 0 9.8-2.7 12-7.8l3 1.1c-2.7 6.7-8.8 11-15 11-3.5 0-7.1-1.2-10-3.7L4 36v-7h7Zm6-16.5C12.8 11.5 9 14 6.8 18L4 16.8C6.5 10.2 12.7 6 19 6c4.1 0 7.8 1.2 10.5 3.4L32 4v7h-7l2.7-2.1C26.5 8 23.2 7 20 7.5Z'
    }
  ];

  const stats = [
    { value: '120+', label: 'Projects Delivered' },
    { value: '18+', label: 'Industry Sectors' },
    { value: '99%', label: 'Client Satisfaction' },
    { value: '5+', label: 'Years Experience' }
  ];

  const avatars = [
    { initials: 'AL' },
    { initials: 'MK' },
    { initials: 'SP' },
    { initials: 'JN' }
  ];

  let projectCount = $state(128);

  const incrementProjectCount = (amount: number) => {
    projectCount += amount;
  };
</script>

<svelte:head>
  <title>Northstar Studio | Home</title>
  <meta name="description" content="Northstar Studio creates premium digital experiences that drive real results." />
</svelte:head>

<section class="relative overflow-hidden bg-[#050B1F]">
  <div class="absolute inset-0 -z-10 bg-[radial-gradient(circle_at_top_left,rgba(56,189,248,0.18),transparent_24%),radial-gradient(circle_at_80%_15%,rgba(168,85,247,0.18),transparent_22%),linear-gradient(180deg,#050B1F_0%,#071024_45%,#0B1120_100%)]"></div>
  <div class="mx-auto max-w-7xl px-4 py-16 sm:px-6 lg:px-8 lg:py-24">
    <div class="grid items-center gap-14 lg:grid-cols-[1.02fr_0.98fr]">
      <div>
        <div class="inline-flex items-center rounded-full border border-white/10 bg-white/5 px-4 py-2 text-xs font-semibold uppercase tracking-[0.45em] text-sky-200 shadow-lg shadow-sky-500/10">
          We build digital solutions
        </div>

        <h1 class="mt-7 max-w-3xl text-5xl font-bold tracking-tight text-white sm:text-6xl lg:text-7xl lg:leading-[1.02]">
          We create digital experiences that <span class="bg-gradient-to-r from-sky-300 via-cyan-300 to-violet-300 bg-clip-text text-transparent">drive real results</span>.
        </h1>

        <p class="mt-6 max-w-2xl text-lg leading-8 text-slate-300 sm:text-xl">
          Northstar Studio designs premium websites that blend strategy, performance, and clarity into one cohesive experience for modern companies.
        </p>

        <div class="mt-9 flex flex-col gap-4 sm:flex-row">
          <a href={resolve('/contact')} class="inline-flex items-center justify-center rounded-full bg-gradient-to-r from-sky-400 to-violet-500 px-7 py-3.5 text-sm font-semibold text-white shadow-[0_18px_45px_rgba(56,189,248,0.25)] transition duration-300 hover:-translate-y-0.5 hover:shadow-[0_24px_60px_rgba(56,189,248,0.3)]">
            Get Started
          </a>
          <a href={resolve('/about')} class="inline-flex items-center justify-center rounded-full border border-white/12 bg-white/5 px-7 py-3.5 text-sm font-semibold text-white backdrop-blur transition duration-300 hover:-translate-y-0.5 hover:border-sky-400/40 hover:bg-white/10">
            View Our Work
          </a>
        </div>

        <div class="mt-10 flex flex-col gap-5 sm:flex-row sm:items-center sm:gap-6">
          <div class="flex items-center -space-x-3">
            {#each avatars as avatar (avatar.initials)}
              <div class="flex h-11 w-11 items-center justify-center rounded-full border-2 border-slate-950 bg-gradient-to-br from-white to-slate-200 text-xs font-bold text-slate-900 shadow-lg shadow-black/20">
                {avatar.initials}
              </div>
            {/each}
          </div>

          <div>
            <div class="flex items-center gap-1 text-amber-300">
              {#each stars as star (star)}
                <span>★</span>
              {/each}
            </div>
            <p class="mt-2 text-sm text-slate-300">Trusted by 100+ clients worldwide</p>
          </div>
        </div>
      </div>

      <div class="relative">
        <div class="absolute -inset-8 rounded-[2.5rem] bg-gradient-to-br from-sky-400/20 via-violet-500/20 to-cyan-400/15 blur-3xl"></div>
        <div class="relative overflow-hidden rounded-[2rem] border border-white/10 bg-white/[0.04] p-5 shadow-[0_30px_120px_rgba(2,6,23,0.45)] backdrop-blur-xl">
          <div class="grid gap-4 sm:grid-cols-[1.1fr_0.9fr]">
            <div class="rounded-[1.75rem] border border-white/10 bg-slate-950/70 p-5 shadow-[0_20px_60px_rgba(2,6,23,0.2)]">
              <div class="flex items-center justify-between">
                <div>
                  <p class="text-xs uppercase tracking-[0.4em] text-slate-400">Dashboard</p>
                  <p class="mt-2 text-xl font-bold text-white">Campaign Overview</p>
                </div>
                <div class="rounded-full bg-emerald-400/10 px-3 py-1 text-xs font-semibold text-emerald-300">+18.4%</div>
              </div>

              <div class="mt-6 rounded-[1.5rem] border border-white/10 bg-gradient-to-br from-sky-400/15 via-cyan-400/10 to-violet-500/10 p-4">
                <div class="flex items-center justify-between text-sm text-slate-300">
                  <span>Monthly growth</span>
                  <span>58%</span>
                </div>
                <div class="mt-4 grid h-36 grid-cols-6 items-end gap-2">
                  <div class="h-14 rounded-t-xl bg-gradient-to-t from-sky-500 to-cyan-400"></div>
                  <div class="h-20 rounded-t-xl bg-gradient-to-t from-sky-500 to-cyan-400"></div>
                  <div class="h-10 rounded-t-xl bg-gradient-to-t from-sky-500 to-cyan-400"></div>
                  <div class="h-28 rounded-t-xl bg-gradient-to-t from-violet-500 to-fuchsia-400"></div>
                  <div class="h-18 rounded-t-xl bg-gradient-to-t from-sky-500 to-cyan-400"></div>
                  <div class="h-32 rounded-t-xl bg-gradient-to-t from-violet-500 to-fuchsia-400"></div>
                </div>
              </div>

              <div class="mt-4 grid gap-3 sm:grid-cols-2">
                <div class="rounded-[1.25rem] border border-white/10 bg-white/5 p-4">
                  <p class="text-xs uppercase tracking-[0.35em] text-slate-500">Leads</p>
                  <p class="mt-3 text-2xl font-bold text-white">1,284</p>
                </div>
                <div class="rounded-[1.25rem] border border-white/10 bg-white/5 p-4">
                  <p class="text-xs uppercase tracking-[0.35em] text-slate-500">Conversion</p>
                  <p class="mt-3 text-2xl font-bold text-white">6.8%</p>
                </div>
              </div>
            </div>

            <div class="space-y-4">
              <div class="rounded-[1.5rem] border border-white/10 bg-slate-950/70 p-5 shadow-[0_20px_60px_rgba(2,6,23,0.18)]">
                <div class="flex items-center justify-between">
                  <div>
                    <p class="text-xs uppercase tracking-[0.35em] text-slate-500">Project counter</p>
                    <p class="mt-2 text-4xl font-bold text-white">{projectCount}</p>
                  </div>
                  <div class="rounded-2xl bg-sky-400/10 p-3 text-sky-300">◆</div>
                </div>
                <p class="mt-3 text-sm leading-6 text-slate-300">A small Svelte reactivity example that updates instantly.</p>
                <div class="mt-5 flex flex-wrap gap-3">
                  <button type="button" class="rounded-full bg-white px-4 py-2.5 text-sm font-semibold text-slate-950 transition duration-300 hover:-translate-y-0.5" onclick={() => incrementProjectCount(1)}>
                    +1 project
                  </button>
                  <button type="button" class="rounded-full border border-white/10 bg-white/5 px-4 py-2.5 text-sm font-semibold text-white transition duration-300 hover:-translate-y-0.5 hover:border-sky-400/40 hover:bg-white/10" onclick={() => incrementProjectCount(5)}>
                    +5 projects
                  </button>
                </div>
              </div>

              <div class="rounded-[1.5rem] border border-white/10 bg-white/5 p-5 shadow-[0_20px_60px_rgba(2,6,23,0.18)]">
                <p class="text-xs uppercase tracking-[0.35em] text-slate-500">Highlights</p>
                <div class="mt-4 space-y-3">
                  <div class="flex items-center justify-between rounded-2xl bg-white/5 px-4 py-3 text-sm text-slate-300">
                    <span>Delivery model</span>
                    <span class="font-semibold text-white">Fast and structured</span>
                  </div>
                  <div class="flex items-center justify-between rounded-2xl bg-white/5 px-4 py-3 text-sm text-slate-300">
                    <span>Support style</span>
                    <span class="font-semibold text-white">Clear and proactive</span>
                  </div>
                </div>
              </div>

              <div class="grid grid-cols-3 gap-3">
                <div class="rounded-[1.25rem] border border-white/10 bg-white/5 p-4 text-center">
                  <p class="text-2xl font-bold text-white">24</p>
                  <p class="mt-1 text-xs uppercase tracking-[0.3em] text-slate-500">Tasks</p>
                </div>
                <div class="rounded-[1.25rem] border border-white/10 bg-white/5 p-4 text-center">
                  <p class="text-2xl font-bold text-white">8</p>
                  <p class="mt-1 text-xs uppercase tracking-[0.3em] text-slate-500">Widgets</p>
                </div>
                <div class="rounded-[1.25rem] border border-white/10 bg-white/5 p-4 text-center">
                  <p class="text-2xl font-bold text-white">92</p>
                  <p class="mt-1 text-xs uppercase tracking-[0.3em] text-slate-500">Score</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="mx-auto max-w-7xl px-4 pb-16 sm:px-6 lg:px-8 lg:pb-24">
  <div class="rounded-[2rem] border border-slate-200/80 bg-white px-6 py-8 shadow-[0_24px_80px_rgba(15,23,42,0.08)] sm:px-8">
    <div class="grid gap-4 sm:grid-cols-2 lg:grid-cols-5 lg:items-center">
      {#each trustedCompanies as company (company)}
        <div class="rounded-[1.25rem] border border-slate-200 bg-slate-50 px-4 py-4 text-center text-sm font-semibold uppercase tracking-[0.35em] text-slate-500 transition duration-300 hover:-translate-y-0.5 hover:border-sky-200 hover:bg-sky-50">
          {company}
        </div>
      {/each}
    </div>
  </div>
</section>

<section class="mx-auto max-w-7xl px-4 pb-16 sm:px-6 lg:px-8 lg:pb-24">
  <div class="flex flex-col gap-4 md:flex-row md:items-end md:justify-between">
    <div>
      <p class="text-sm font-semibold uppercase tracking-[0.45em] text-sky-300">Services</p>
      <h2 class="mt-3 max-w-3xl text-3xl font-bold tracking-tight text-white sm:text-4xl">Everything you need for a digital presence</h2>
    </div>
    <p class="max-w-2xl text-sm leading-6 text-slate-400">
      From strategic design to launch-ready development, every section is crafted to feel premium, fast, and easy to trust.
    </p>
  </div>

  <div class="mt-10 grid gap-6 lg:grid-cols-2">
    {#each services as service (service.badge)}
      <ServiceCard {...service} />
    {/each}
  </div>
</section>

<section class="mx-auto max-w-7xl px-4 pb-20 sm:px-6 lg:px-8 lg:pb-28">
  <div class="rounded-[2rem] border border-white/10 bg-slate-950/80 px-6 py-10 shadow-[0_30px_100px_rgba(2,6,23,0.3)] sm:px-8 lg:px-10">
    <div class="grid gap-6 md:grid-cols-4">
      {#each stats as stat (stat.label)}
        <div class="rounded-[1.5rem] border border-white/10 bg-white/5 p-6 text-center transition duration-300 hover:-translate-y-1 hover:bg-white/[0.08]">
          <p class="text-4xl font-bold tracking-tight text-white sm:text-5xl">{stat.value}</p>
          <p class="mt-3 text-sm uppercase tracking-[0.3em] text-slate-400">{stat.label}</p>
        </div>
      {/each}
    </div>
  </div>
</section>
