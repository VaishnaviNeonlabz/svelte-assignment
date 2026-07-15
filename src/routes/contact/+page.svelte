<script lang="ts">
  type FormErrors = {
    name?: string;
    email?: string;
    message?: string;
  };

  let name = $state('');
  let email = $state('');
  let message = $state('');
  let errors = $state<FormErrors>({});
  let successMessage = $state('');

  const validateEmail = (value: string) => /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(value);

  const validateForm = () => {
    const nextErrors: FormErrors = {};

    if (!name.trim()) {
      nextErrors.name = 'Please enter your name.';
    }

    if (!email.trim()) {
      nextErrors.email = 'Please enter your email address.';
    } else if (!validateEmail(email)) {
      nextErrors.email = 'Please enter a valid email address.';
    }

    if (!message.trim()) {
      nextErrors.message = 'Please share a few details about your project.';
    }

    errors = nextErrors;
    return Object.keys(nextErrors).length === 0;
  };

  const handleSubmit = (event: SubmitEvent) => {
    event.preventDefault();
    successMessage = '';

    if (!validateForm()) {
      return;
    }

    successMessage = 'Thanks. Your message has been prepared successfully and we will respond soon.';
    name = '';
    email = '';
    message = '';
    errors = {};
  };
</script>

<svelte:head>
  <title>Northstar Studio | Contact</title>
  <meta name="description" content="Contact Northstar Studio with your name, email, and message." />
</svelte:head>

<section class="relative overflow-hidden bg-[#050B1F]">
  <div class="absolute inset-0 -z-10 bg-[radial-gradient(circle_at_top_left,rgba(56,189,248,0.18),transparent_24%),radial-gradient(circle_at_80%_18%,rgba(168,85,247,0.16),transparent_22%),linear-gradient(180deg,#050B1F_0%,#071024_45%,#0B1120_100%)]"></div>
  <div class="mx-auto max-w-7xl px-4 py-16 sm:px-6 lg:px-8 lg:py-24">
    <div class="max-w-3xl">
      <div class="inline-flex rounded-full border border-white/10 bg-white/5 px-4 py-2 text-xs font-semibold uppercase tracking-[0.45em] text-sky-200 shadow-lg shadow-sky-500/10">
        Contact Northstar Studio
      </div>
      <h1 class="mt-6 text-5xl font-bold tracking-tight text-white sm:text-6xl lg:text-7xl lg:leading-[1.02]">
        Let&apos;s work together
      </h1>
      <p class="mt-6 max-w-2xl text-lg leading-8 text-slate-300 sm:text-xl">
        Reach out with a project idea, timeline, or question. We&apos;ll review your message and respond with a practical next step.
      </p>
    </div>
  </div>
</section>

<section class="mx-auto max-w-7xl px-4 pb-16 sm:px-6 lg:px-8 lg:pb-24">
  <div class="grid gap-10 lg:grid-cols-[0.95fr_1.05fr] lg:items-start">
    <div class="rounded-[2rem] border border-white/10 bg-white/5 p-8 shadow-[0_24px_80px_rgba(2,6,23,0.24)] backdrop-blur-xl sm:p-10">
      <p class="text-xs font-semibold uppercase tracking-[0.45em] text-sky-300">Contact Information</p>
      <h2 class="mt-4 text-4xl font-bold tracking-tight text-white sm:text-5xl">We&apos;re here to help!</h2>
      <p class="mt-5 max-w-xl text-base leading-7 text-slate-300 sm:text-lg">
        Talk to us about design, development, branding, or a launch plan. We keep the process clear, responsive, and easy to follow.
      </p>

      <div class="mt-10 space-y-4">
        <div class="flex min-w-0 items-start gap-4 rounded-2xl border border-white/10 bg-slate-950/45 p-4 transition duration-300 hover:-translate-y-0.5 hover:border-sky-400/30 hover:bg-slate-950/60">
          <div class="flex h-12 w-12 shrink-0 items-center justify-center rounded-2xl bg-sky-400/10 text-sky-300">
            <svg viewBox="0 0 24 24" class="h-5 w-5 fill-none stroke-current stroke-[1.8]" aria-hidden="true">
              <path d="M4 6h16v12H4z"></path>
              <path d="m4 7 8 6 8-6"></path>
            </svg>
          </div>
          <div class="min-w-0 flex-1">
            <p class="text-sm font-semibold uppercase tracking-[0.3em] text-slate-400">Email</p>
            <a href="mailto:hello@northstarstudio.lk" class="mt-1 block min-w-0 break-all text-base font-medium text-white transition hover:text-sky-200">
              hello@northstarstudio.lk
            </a>
          </div>
        </div>

        <div class="flex min-w-0 items-start gap-4 rounded-2xl border border-white/10 bg-slate-950/45 p-4 transition duration-300 hover:-translate-y-0.5 hover:border-sky-400/30 hover:bg-slate-950/60">
          <div class="flex h-12 w-12 shrink-0 items-center justify-center rounded-2xl bg-cyan-400/10 text-cyan-300">
            <svg viewBox="0 0 24 24" class="h-5 w-5 fill-none stroke-current stroke-[1.8]" aria-hidden="true">
              <path d="M6.6 10.8c1.2 2.2 2.8 3.8 5 5l1.7-1.7a1 1 0 0 1 1-.2c1 .3 2 .5 3.1.5a1 1 0 0 1 1 1V19a1 1 0 0 1-1 1C10.4 20 4 13.6 4 5.6a1 1 0 0 1 1-1h3.6a1 1 0 0 1 1 1c0 1.1.2 2.1.5 3.1a1 1 0 0 1-.2 1l-1.3 1.1Z"></path>
            </svg>
          </div>
          <div class="min-w-0 flex-1">
            <p class="text-sm font-semibold uppercase tracking-[0.3em] text-slate-400">Phone</p>
            <p class="mt-1 text-base font-medium text-white">+94 76 123 4567</p>
          </div>
        </div>

        <div class="flex min-w-0 items-start gap-4 rounded-2xl border border-white/10 bg-slate-950/45 p-4 transition duration-300 hover:-translate-y-0.5 hover:border-sky-400/30 hover:bg-slate-950/60">
          <div class="flex h-12 w-12 shrink-0 items-center justify-center rounded-2xl bg-indigo-400/10 text-indigo-300">
            <svg viewBox="0 0 24 24" class="h-5 w-5 fill-none stroke-current stroke-[1.8]" aria-hidden="true">
              <path d="M12 21s6-5.5 6-11a6 6 0 0 0-12 0c0 5.5 6 11 6 11Z"></path>
              <path d="M12 10.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3Z"></path>
            </svg>
          </div>
          <div class="min-w-0 flex-1">
            <p class="text-sm font-semibold uppercase tracking-[0.3em] text-slate-400">Address</p>
            <p class="mt-1 text-base font-medium text-white">Colombo, Sri Lanka</p>
          </div>
        </div>

        <div class="flex min-w-0 items-start gap-4 rounded-2xl border border-white/10 bg-slate-950/45 p-4 transition duration-300 hover:-translate-y-0.5 hover:border-sky-400/30 hover:bg-slate-950/60">
          <div class="flex h-12 w-12 shrink-0 items-center justify-center rounded-2xl bg-violet-400/10 text-violet-300">
            <svg viewBox="0 0 24 24" class="h-5 w-5 fill-none stroke-current stroke-[1.8]" aria-hidden="true">
              <path d="M7 4h10v6H7z"></path>
              <path d="M6 16h12"></path>
              <path d="M8 20h8"></path>
            </svg>
          </div>
          <div class="min-w-0 flex-1">
            <p class="text-sm font-semibold uppercase tracking-[0.3em] text-slate-400">Business Hours</p>
            <p class="mt-1 text-base font-medium text-white">Mon - Fri, 9:00 AM - 6:00 PM</p>
          </div>
        </div>

        <div class="flex min-w-0 items-start gap-4 rounded-2xl border border-white/10 bg-slate-950/45 p-4 transition duration-300 hover:-translate-y-0.5 hover:border-sky-400/30 hover:bg-slate-950/60">
          <div class="flex h-12 w-12 shrink-0 items-center justify-center rounded-2xl bg-emerald-400/10 text-emerald-300">
            <svg viewBox="0 0 24 24" class="h-5 w-5 fill-none stroke-current stroke-[1.8]" aria-hidden="true">
              <path d="M12 20a8 8 0 1 0-8-8"></path>
              <path d="M12 6v6l4 2"></path>
            </svg>
          </div>
          <div class="min-w-0 flex-1">
            <p class="text-sm font-semibold uppercase tracking-[0.3em] text-slate-400">Response Time</p>
            <p class="mt-1 text-base font-medium text-white">Usually within one business day</p>
          </div>
        </div>
      </div>
    </div>

    <div class="rounded-[2rem] border border-white/10 bg-slate-900/80 p-6 shadow-[0_24px_90px_rgba(2,6,23,0.34)] backdrop-blur-xl sm:p-8">
      <div class="mb-8 border-b border-white/10 pb-6">
        <p class="text-xs font-semibold uppercase tracking-[0.45em] text-sky-300">Send a message</p>
        <h2 class="mt-3 text-2xl font-bold tracking-tight text-white sm:text-3xl">We usually reply within one business day.</h2>
        <p class="mt-3 max-w-xl text-sm leading-6 text-slate-400 sm:text-base">
          Share a few details and we&apos;ll come back with a useful next step.
        </p>
      </div>

      <form class="space-y-5" onsubmit={handleSubmit}>
        <div>
          <label class="mb-2 block text-sm font-medium text-slate-200" for="name">Name</label>
          <input id="name" type="text" bind:value={name} class="w-full rounded-[1.4rem] border border-white/10 bg-white/5 px-4 py-3.5 text-white outline-none transition placeholder:text-slate-500 focus:border-sky-400/60 focus:bg-white/[0.07] focus:ring-2 focus:ring-sky-400/20" placeholder="Your name" />
          {#if errors.name}
            <p class="mt-2 rounded-2xl border border-rose-400/20 bg-rose-400/10 px-4 py-2 text-sm text-rose-200">{errors.name}</p>
          {/if}
        </div>

        <div>
          <label class="mb-2 block text-sm font-medium text-slate-200" for="email">Email</label>
          <input id="email" type="email" bind:value={email} class="w-full rounded-[1.4rem] border border-white/10 bg-white/5 px-4 py-3.5 text-white outline-none transition placeholder:text-slate-500 focus:border-sky-400/60 focus:bg-white/[0.07] focus:ring-2 focus:ring-sky-400/20" placeholder="you@example.com" />
          {#if errors.email}
            <p class="mt-2 rounded-2xl border border-rose-400/20 bg-rose-400/10 px-4 py-2 text-sm text-rose-200">{errors.email}</p>
          {/if}
        </div>

        <div>
          <label class="mb-2 block text-sm font-medium text-slate-200" for="message">Message</label>
          <textarea id="message" rows="6" bind:value={message} class="w-full rounded-[1.4rem] border border-white/10 bg-white/5 px-4 py-3.5 text-white outline-none transition placeholder:text-slate-500 focus:border-sky-400/60 focus:bg-white/[0.07] focus:ring-2 focus:ring-sky-400/20" placeholder="Tell us about your project goals, timeline, or current challenges"></textarea>
          {#if errors.message}
            <p class="mt-2 rounded-2xl border border-rose-400/20 bg-rose-400/10 px-4 py-2 text-sm text-rose-200">{errors.message}</p>
          {/if}
        </div>

        <button type="submit" class="inline-flex w-full items-center justify-center rounded-full bg-gradient-to-r from-sky-400 to-violet-500 px-6 py-3.5 text-sm font-semibold text-white shadow-[0_18px_45px_rgba(56,189,248,0.24)] transition duration-300 hover:-translate-y-0.5 hover:shadow-[0_24px_60px_rgba(56,189,248,0.3)]">
          Send Message
        </button>

        {#if successMessage}
          <p class="rounded-[1.4rem] border border-emerald-400/20 bg-emerald-400/10 px-4 py-3 text-sm text-emerald-200" aria-live="polite">
            {successMessage}
          </p>
        {/if}
      </form>
    </div>
  </div>
</section>

<section class="mx-auto max-w-7xl px-4 pb-20 sm:px-6 lg:px-8 lg:pb-28">
  <div class="rounded-[2rem] border border-white/10 bg-white p-4 shadow-[0_24px_80px_rgba(15,23,42,0.12)] sm:p-6">
    <div class="overflow-hidden rounded-[1.5rem] border border-slate-200">
      <iframe title="Google map showing Colombo, Sri Lanka" src="https://www.google.com/maps?q=Colombo,%20Sri%20Lanka&output=embed" class="h-[420px] w-full" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </div>
  </div>
</section>
