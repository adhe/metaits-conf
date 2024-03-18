<script>
	import Link from '$lib/components/Link.svelte';
	import Logo from '$lib/assets/metaits-logo.jpg';

	export let url;
	// let lastScrollPosition = 0;
	let isNavAppear = false;

	function handleScroll () {
	// console.log(window.pageYOffset)

		const currentScrollPosition = window.scrollY || document.documentElement.scrollTop;
		if (currentScrollPosition > 600) {
			console.log('Navbar appear')
			isNavAppear = true;
		} else {
			console.log('nav delete')
			isNavAppear = false;
		}

	}
</script>

<svelte:window on:scroll={handleScroll} />

<div class={`${isNavAppear ? 'ease-out' : '-translate-y-full ease-in-out'} fixed top-0 inset-x-0 drop-shadow-md  backdrop-blur-xl bg-white/85 transition duration-300 z-10`}>
	<div class="container flex items-center justify-between py-3 mx-auto">
		<img src={Logo} class="h-16 w-96 object-cover" alt="" />
		<div class="flex">
			<Link href={url}>Home</Link>
			<Link href={url + '/call-for-paper'}>Call for Paper</Link>
			<Link href={url + '/keynote'}>Keynote Speaker</Link>
			<Link href={url + '/submissions'}>Submissions</Link>
			<Link href={url + '/registration'}>Registration</Link>
			<Link href={url + '/contact'}>Contact</Link>
		</div>
	</div>
</div>
