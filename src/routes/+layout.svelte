<script>
	let pages = [
		{
			name: 'Home',
			path: '/'
		},
		{
			name: 'About',
			path: '/about'
		},
		{
			name: 'Services',
			path: '/services'
		},
		{
			name: 'Contact',
			path: '/contact'
		}
	];

	let legalPages = [
		{
			name: 'Privacy Policy',
			path: '/legal/privacy-policy'
		},
		{
			name: 'Terms of Service',
			path: '/legal/terms-of-service'
		},
		{
			name: 'Disclaimer',
			path: '/legal/disclaimer'
		}
	];
</script>

<header>
	<a class="skip-link" href="#main-content" aria-label="Skip to main content"
		>Skip to main content</a
	>
	<div class="logo logo--primary">
		<span class="logo__text">My Website Logo</span>
	</div>
	<nav class="nav" aria-label="Main Navigation">
		<ul class="nav__list">
			{#each pages as page}
				<li class="nav__item">
					<a href={page.path} class="nav__link" aria-current="page">{page.name}</a>
				</li>
			{/each}
		</ul>
	</nav>
</header>

<main id="main-content" class="page-content">
	<slot />
</main>

<footer class="footer">
	<nav class="nav nav--footer" aria-label="Footer Navigation">
		<ul class="nav__list">
			{#each pages as page}
				<li class="nav__item"><a href={page.path} class="nav__link">{page.name}</a></li>
			{/each}
		</ul>
	</nav>
	<nav class="nav nav--legal" aria-label="Legal Navigation">
		<ul class="nav__list">
			{#each legalPages as page}
				<li class="nav__item">
					<a href={page.path} class="nav__link">{page.name}</a>
				</li>
			{/each}
		</ul>
	</nav>
	<div class="footer__copyright">&copy; 2023 Your Company Name. All rights reserved.</div>
</footer>

<style>
	/* To Hide Skip Link */
	.skip-link {
		position: absolute;
		top: -40px;
		left: 0;
		background-color: #fff;
		color: #000;
		padding: 5px 10px;
		z-index: 9999;
		overflow: hidden;
		clip: rect(0, 0, 0, 0);
		width: 1px;
		height: 1px;
	}
</style>
