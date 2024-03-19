<script>
	import Link from '$lib/components/Link.svelte';

	export let url;
	let isNavAppear = false;

	function handleScroll () {
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
	<div class="container w-4/5 flex items-center justify-between py-3 mx-auto">
		<img src="metaits-logo-black.svg" class="h-12 " alt="" />
		<div class="flex">
			<Link href={url + '#'}>Home</Link>
			<Link href={url + '/#topic'}>Topics</Link>
			<Link href={url + '/#keynote-speaker'}>Keynote Speaker</Link>
			<Link href={url + '/#submissions'}>Submissions</Link>
			<Link href={url + '/#'}>Registration</Link>
			<Link href={url + '/#contact'}>Contact</Link>
		</div>
	</div>
</div>
