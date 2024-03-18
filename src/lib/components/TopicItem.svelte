<script>
	export let data;
</script>

<div class="bg-teal-950 rounded-2xl px-6 py-5 text-white">
	<div class="text-2xl font-medium w-4/5 leading-tight">{data?.title}</div>
	<ul class="list-disc px-4 opacity-75 mt-4">
		{#each data?.items as item}
			<li>{item}</li>
		{/each}
	</ul>
</div>
