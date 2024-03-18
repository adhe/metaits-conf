<script>
	import '../app.css';
	import { PUBLIC_URL } from '$env/static/public';
	import Nav from '$lib/components/Nav.svelte';

	let url = '';

	$: url = import.meta.env.MODE === 'production' ? PUBLIC_URL : 'http://localhost:5173';
</script>

<Nav {url}></Nav>
<slot />
