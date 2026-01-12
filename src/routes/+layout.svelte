<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import Navbar from '$lib/components/Navbar.svelte';
	import Footer from '$lib/components/Footer.svelte';

	import { page } from '$app/state';

	let { children } = $props();

	const siteTitle = 'Ko-Dingin | Jasa Joki Tugas Coding & IT Terpercaya';
	const siteDescription = 'Joki tugas coding profesional...';
	const siteUrl = 'https://ko-dingin.com';
	const siteImage = `${siteUrl}/og-image.jpg`;
	const siteKeywords = 'joki tugas coding, jasa pembuatan program...';
</script>

<svelte:head>
	<title>{siteTitle}</title>
	<meta name="description" content={siteDescription} />
	<meta name="keywords" content={siteKeywords} />
	<meta name="author" content="Ko-Dingin Team" />
	<meta name="robots" content="index, follow" />
	<link rel="icon" href={favicon} />

	<link rel="canonical" href={page.url.href} />

	<meta property="og:type" content="website" />
	<meta property="og:url" content={page.url.href} />
	<meta property="og:title" content={siteTitle} />
	<meta property="og:description" content={siteDescription} />
	<meta property="og:image" content={siteImage} />
	<meta property="og:site_name" content="Ko-Dingin" />
	<meta property="og:locale" content="id_ID" />

	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:url" content={page.url.href} />
	<meta name="twitter:title" content={siteTitle} />
	<meta name="twitter:description" content={siteDescription} />
	<meta name="twitter:image" content={siteImage} />

	{@html `<script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "ProfessionalService",
      "name": "Ko-Dingin",
      "image": "${siteImage}",
      "description": "${siteDescription}",
      "url": "${siteUrl}",
      "priceRange": "$$",
      "address": {
        "@type": "PostalAddress",
        "addressCountry": "ID"
      }
    }
  </script>`}
</svelte:head>

<div class="flex min-h-screen flex-col font-sans">
	<Navbar />

	<main class="grow">
		{@render children()}
	</main>

	<Footer />
</div>
