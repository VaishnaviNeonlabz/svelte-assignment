<script lang="ts">
  type Props = {
    badge: string;
    title: string;
    description: string;
    features: string[];
    accent: string;
    icon: string;
  };

  let { badge, title, description, features = [], accent, icon }: Props = $props();
</script>

<article
  class={`group relative overflow-hidden rounded-[2rem] border border-white/10 bg-white/5 p-7 shadow-[0_24px_80px_rgba(2,6,23,0.28)] transition duration-300 hover:-translate-y-1 hover:border-sky-400/40 hover:shadow-[0_28px_90px_rgba(59,130,246,0.16)] ${accent}`}
>
  <div class="absolute right-0 top-0 h-32 w-32 translate-x-1/2 -translate-y-1/2 rounded-full bg-white/10 blur-3xl transition duration-300 group-hover:bg-sky-400/10"></div>

  <div class="flex items-start justify-between gap-4">
    <div class="flex h-14 w-14 items-center justify-center rounded-2xl border border-white/10 bg-slate-950/40 text-white shadow-lg shadow-black/10 transition duration-300 group-hover:scale-105">
      <svg viewBox="0 0 48 48" class="h-6 w-6 fill-current" aria-hidden="true">
        <path d={icon}></path>
      </svg>
    </div>
    <div class="rounded-full border border-white/10 bg-white/5 px-3 py-1 text-[0.7rem] font-semibold uppercase tracking-[0.35em] text-slate-300">
      {badge}
    </div>
  </div>

  <h3 class="mt-8 text-2xl font-bold tracking-tight text-white">{title}</h3>
  <p class="mt-4 text-sm leading-7 text-slate-300">{description}</p>

  <div class="mt-7 space-y-3">
    {#each features as feature (feature)}
      <div class="flex items-center gap-3 text-sm text-slate-200">
        <span class="h-2 w-2 rounded-full bg-gradient-to-r from-sky-400 to-cyan-400 shadow-[0_0_12px_rgba(56,189,248,0.6)]"></span>
        <span>{feature}</span>
      </div>
    {/each}
  </div>
</article>
