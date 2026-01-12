<script>
	const features = [
		{
			icon: '⚡',
			title: 'Kilat & Tepat',
			desc: 'Deadline besok pagi? Tenang. Tim kami terbiasa bergadang (mode malam aktif) untuk menyelamatkan nilaimu.'
		},
		{
			icon: '🔒',
			title: 'Privasi Terjamin',
			desc: 'Identitas aman 100%. Dosen tidak akan tahu, teman tidak akan curiga. Ini rahasia kita berdua.'
		},
		{
			icon: '🧠',
			title: 'Code Rapi & Jelas',
			desc: 'Bukan sekadar copy-paste. Struktur kodingan rapi dengan komentar penjelas, jadi aman saat ditanya dosen.'
		},
		{
			icon: '🔄',
			title: 'Garansi Revisi',
			desc: 'Program error saat demo? Atau ada fitur yang kurang pas? Kami perbaiki gratis sampai program jalan mulus.'
		},
		{
			icon: '💸',
			title: 'Harga Mahasiswa',
			desc: 'Tarif bersahabat dengan kantong akhir bulan. Kualitas sultan, tapi harga tetap standar anak kos.'
		},
		{
			icon: '🤝',
			title: 'Free Konsultasi',
			desc: 'Bingung cara jalanin programnya? Kami pandu step-by-step sampai kamu paham cara kerjanya.'
		}
	];
</script>

<section id="features" class="relative bg-base-100 py-24">
	<div class="container mx-auto px-6">
		<div class="mx-auto mb-16 max-w-2xl text-center">
			<h2 class="mb-4 text-3xl font-bold text-base-content md:text-4xl">Kenapa Pilih Ko-Dingin?</h2>
			<p class="text-lg text-base-content/60">
				Solusi coding malam hari tanpa drama, biar kamu bisa tidur nyenyak.
			</p>
		</div>

		<div class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
			{#each features as feature}
				<div
					class="group card border border-base-300 bg-base-200 shadow-sm transition-all duration-300 hover:-translate-y-1 hover:shadow-xl hover:shadow-primary/20"
				>
					<div class="card-body items-center p-8 text-center">
						<div
							class="mb-6 flex h-16 w-16 items-center justify-center rounded-2xl bg-primary/10 text-3xl text-primary transition-colors group-hover:bg-primary group-hover:text-primary-content"
						>
							{feature.icon}
						</div>

						<h3 class="mb-3 card-title text-xl font-bold text-base-content">
							{feature.title}
						</h3>

						<p class="leading-relaxed text-base-content/70">
							{feature.desc}
						</p>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
