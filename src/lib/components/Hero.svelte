<script>
	const snowflakes = Array.from({ length: 50 }).map((_, i) => ({
		id: i,
		left: Math.random() * 100 + '%',
		animationDuration: Math.random() * 10 + 8 + 's',
		animationDelay: '-' + Math.random() * 10 + 's',
		opacity: Math.random() * 0.5 + 0.3,
		size: Math.random() * 14 + 14 + 'px',
		initialRotation: Math.random() * 360 + 'deg'
	}));
</script>

<section class="relative hero min-h-[85vh] overflow-hidden bg-base-200">
	<div
		class="absolute top-[-10%] right-[-5%] h-96 w-96 rounded-full bg-secondary opacity-60 blur-3xl"
	></div>
	<div
		class="absolute bottom-[-10%] left-[-5%] h-72 w-72 rounded-full bg-accent/20 opacity-50 blur-3xl"
	></div>

	<div class="pointer-events-none absolute inset-0 z-0 text-white/70">
		{#each snowflakes as flake (flake.id)}
			<svg
				viewBox="0 0 24 24"
				fill="none"
				xmlns="http://www.w3.org/2000/svg"
				class="animate-snow-spin absolute"
				style="
            left: {flake.left};
            width: {flake.size};
            height: {flake.size};
            opacity: {flake.opacity};
            animation-duration: {flake.animationDuration};
            animation-delay: {flake.animationDelay};
            transform: rotate({flake.initialRotation});
        "
			>
				<circle cx="12" cy="12" r="3" stroke="currentColor" stroke-width="2" />
				<path
					d="M12 8V6M12 3V6M12 6L9 4M12 6L15 4"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
				/>
				<path
					d="M16 12L18 12M21 12L18 12M18 12L20 9M18 12L20 15"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
				/>
				<path
					d="M12 16V18M12 21V18M12 18L9 20M12 18L15 20"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
				/>
				<path
					d="M8 12L6 12M3 12L6 12M6 12L4 9M6 12L4 15"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
				/>
			</svg>
		{/each}
	</div>

	<div class="hero-content z-10 px-4 text-center">
		<div class="max-w-3xl">
			<div
				class="mb-6 badge inline-block rounded-full font-medium text-secondary-content/80 badge-secondary"
			>
				✨ Tugas numpuk? Chill aja.
			</div>

			<h1 class="mb-6 text-5xl leading-tight font-extrabold md:text-7xl">
				Tugas Panas?<br />
				Biar Kami yang
				<span class="bg-linear-to-r from-primary to-accent bg-clip-text text-primary"
					>Dinginkan.</span
				>
			</h1>

			<p class="mx-auto mb-8 max-w-2xl py-4 text-lg leading-relaxed md:text-xl">
				Joki tugas profesional, aman, dan terpercaya. Fokuslah istirahat, biarkan expert kami
				membereskan logika, makalah, dan deadline-mu.
			</p>

			<div class="flex flex-col items-center justify-center gap-4 sm:flex-row">
				<a
					href="#contact"
					class="btn w-full rounded-full border-none px-8 shadow-xl shadow-primary/30 transition-transform btn-lg btn-primary hover:scale-105 sm:w-auto"
				>
					Order Sekarang
				</a>
				<a
					href="#features"
					class="btn w-full rounded-full border-base-300 px-8 btn-outline btn-lg hover:bg-base-300 sm:w-auto"
				>
					Pelajari Dulu
				</a>
			</div>
		</div>
	</div>
</section>

<style>
	@keyframes snowfall-spin {
		0% {
			transform: translateY(-20vh) translateX(-10px) rotate(0deg);
		}
		100% {
			transform: translateY(120vh) translateX(20px) rotate(360deg);
		}
	}

	.animate-snow-spin {
		animation-name: snowfall-spin;
		animation-timing-function: linear;
		animation-iteration-count: infinite;
	}
</style>
