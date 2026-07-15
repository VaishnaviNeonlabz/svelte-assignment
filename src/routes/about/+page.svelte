<script lang="ts">
  const missionPoints = [
    'Turn ideas into clear and convincing digital experiences.',
    'Build high-performing sites that feel elegant and easy to maintain.'
  ];

  const values = [
    {
      title: 'Mission',
      description: 'We help companies communicate with clarity, confidence, and a design language that feels premium from the first impression.',
      icon: 'M24 6l10 5v8c0 7-4.4 12-11 15-6.6-3-11-8-11-15v-8l12-5Z'
    },
    {
      title: 'Vision',
      description: 'We want to be the team that ambitious brands call when they need simplicity, polish, and a reliable production process.',
      icon: 'M12 15c0-6.6 5.4-12 12-12s12 5.4 12 12-5.4 12-12 12-12-5.4-12-12Z'
    }
  ];

  const timeline = [
    { year: '2019', label: 'Founded' },
    { year: '2020', label: 'Growing Team' },
    { year: '2022', label: '100+ Projects' },
    { year: '2024', label: 'Global Clients' }
  ];

  const stats = [
    { value: '12+', label: 'Years Experience' },
    { value: '48', label: 'Launches Supported' },
    { value: '26', label: 'Brand Systems Built' },
    { value: '100%', label: 'Static Delivery Focus' }
  ];
</script>

<svelte:head>
  <title>Northstar Studio | About</title>
  <meta name="description" content="Learn about Northstar Studio's mission, vision, journey, and company statistics." />
</svelte:head>

<section class="relative overflow-hidden bg-[#050B1F]">
  <div class="absolute inset-0 -z-10 bg-[radial-gradient(circle_at_top_right,rgba(56,189,248,0.16),transparent_22%),radial-gradient(circle_at_15%_80%,rgba(168,85,247,0.16),transparent_20%),linear-gradient(180deg,#050B1F_0%,#071024_45%,#0B1120_100%)]"></div>
  <div class="mx-auto max-w-7xl px-4 py-16 sm:px-6 lg:px-8 lg:py-24">
    <div class="grid items-center gap-12 lg:grid-cols-[1.02fr_0.98fr]">
      <div>
        <div class="inline-flex rounded-full border border-white/10 bg-white/5 px-4 py-2 text-xs font-semibold uppercase tracking-[0.45em] text-sky-200 shadow-lg shadow-sky-500/10">
          About Northstar Studio
        </div>
        <h1 class="mt-6 max-w-3xl text-4xl font-bold tracking-tight text-white sm:text-5xl lg:text-6xl lg:leading-[1.05]">
          We&apos;re a team of creators, thinkers and problem solvers.
        </h1>
        <p class="mt-6 max-w-2xl text-lg leading-8 text-slate-300 sm:text-xl">
          We help businesses turn complexity into clarity through strategy-led design, clean development, and a premium digital presence that feels easy to trust.
        </p>

        <ul class="mt-8 space-y-3 text-sm text-slate-300 sm:text-base">
          {#each missionPoints as point (point)}
            <li class="flex items-start gap-3">
              <span class="mt-1 h-2.5 w-2.5 rounded-full bg-gradient-to-r from-sky-400 to-violet-500 shadow-[0_0_14px_rgba(96,165,250,0.5)]"></span>
              <span>{point}</span>
            </li>
          {/each}
        </ul>
      </div>

      <div class="relative">
        <div class="absolute -inset-6 rounded-[2.5rem] bg-gradient-to-br from-sky-400/20 via-violet-500/20 to-cyan-400/15 blur-3xl"></div>
        <div class="relative overflow-hidden rounded-[2rem] border border-white/10 bg-white/[0.04] p-4 shadow-[0_30px_120px_rgba(2,6,23,0.45)] backdrop-blur-xl">
          <img src="/about-hero.svg" alt="Northstar Studio abstract collaboration illustration" class="h-full w-full rounded-[1.6rem] object-cover" />
          <div class="absolute bottom-5 left-5 rounded-[1.35rem] border border-white/10 bg-slate-950/80 px-4 py-3 shadow-[0_18px_45px_rgba(2,6,23,0.35)] backdrop-blur">
            <p class="text-xs uppercase tracking-[0.35em] text-slate-400">Crafted for growth</p>
            <p class="mt-1 text-lg font-semibold text-white">Modern SaaS feel</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="mx-auto max-w-7xl px-4 pb-16 sm:px-6 lg:px-8 lg:pb-24">
  <div class="grid gap-6 lg:grid-cols-2">
    {#each values as value (value.title)}
      <article class="rounded-[2rem] border border-white/10 bg-white/5 p-8 shadow-[0_24px_80px_rgba(2,6,23,0.22)] transition duration-300 hover:-translate-y-1 hover:border-sky-400/30 hover:bg-white/[0.07]">
        <div class="flex h-14 w-14 items-center justify-center rounded-2xl bg-gradient-to-br from-sky-400/15 via-cyan-400/10 to-violet-500/10 text-sky-200">
          <svg viewBox="0 0 48 48" class="h-6 w-6 fill-current" aria-hidden="true">
            <path d={value.icon}></path>
          </svg>
        </div>
        <h2 class="mt-6 text-3xl font-bold tracking-tight text-white">{value.title}</h2>
        <p class="mt-4 max-w-xl text-base leading-7 text-slate-300">{value.description}</p>
      </article>
    {/each}
  </div>
</section>

<section class="mx-auto max-w-7xl px-4 pb-16 sm:px-6 lg:px-8 lg:pb-24">
  <div class="rounded-[2rem] border border-white/10 bg-white/5 p-8 shadow-[0_24px_80px_rgba(2,6,23,0.24)] backdrop-blur-xl sm:p-10">
    <div class="flex flex-col gap-3 md:flex-row md:items-end md:justify-between">
      <div>
        <p class="text-sm font-semibold uppercase tracking-[0.45em] text-sky-300">Journey Timeline</p>
        <h2 class="mt-3 text-3xl font-bold tracking-tight text-white sm:text-4xl">A focused journey of growth and delivery.</h2>
      </div>
      <p class="max-w-2xl text-sm leading-6 text-slate-400">
        From a small founding team to a reliable digital partner, each stage has shaped how we design and deliver modern company websites.
      </p>
    </div>

    <div class="mt-10 grid gap-4 lg:grid-cols-4">
      {#each timeline as item (item.year)}
        <div class="rounded-[1.5rem] border border-white/10 bg-slate-950/70 p-5 transition duration-300 hover:-translate-y-1 hover:border-sky-400/30 hover:bg-slate-950/90">
          <p class="text-sm font-semibold uppercase tracking-[0.4em] text-sky-200">{item.year}</p>
          <p class="mt-4 text-xl font-bold text-white">{item.label}</p>
          <span class="mt-5 block h-1.5 w-14 rounded-full bg-gradient-to-r from-sky-400 to-violet-500"></span>
        </div>
      {/each}
    </div>
  </div>
</section>

<section class="mx-auto max-w-7xl px-4 pb-20 sm:px-6 lg:px-8 lg:pb-28">
  <div class="rounded-[2rem] border border-white/10 bg-slate-950/85 px-6 py-10 shadow-[0_30px_100px_rgba(2,6,23,0.32)] sm:px-8 lg:px-10">
    <div class="flex flex-col gap-4 md:flex-row md:items-end md:justify-between">
      <div>
        <p class="text-sm font-semibold uppercase tracking-[0.45em] text-sky-300">Statistics</p>
        <h2 class="mt-3 text-3xl font-bold tracking-tight text-white sm:text-4xl">Built to deliver premium results.</h2>
      </div>
      <p class="max-w-xl text-sm leading-6 text-slate-400">
        The numbers below reflect a design and delivery process that stays focused, predictable, and measurable.
      </p>
    </div>

    <div class="mt-10 grid gap-4 sm:grid-cols-2 xl:grid-cols-4">
      {#each stats as stat (stat.label)}
        <div class="rounded-[1.5rem] border border-white/10 bg-white/5 p-6 text-center transition duration-300 hover:-translate-y-1 hover:bg-white/[0.08]">
          <p class="text-4xl font-bold tracking-tight text-white sm:text-5xl">{stat.value}</p>
          <p class="mt-3 text-sm uppercase tracking-[0.3em] text-slate-400">{stat.label}</p>
        </div>
      {/each}
    </div>
  </div>
</section>
