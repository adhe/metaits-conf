<script>
	export let data;
	</script>

<div class="flex space-x-8 py-12">
	<div class="w-1/4">
		<img src={data?.photoUrl} class="w-full h-80 object-cover rounded-2xl" alt="">
	</div>
	<div class="flex-1 text-white">
		<div class="text-4xl font-medium">{data?.name}</div>
		<div class="opacity-75 text-lg">{data?.university}</div>

		<div class="border-t w-1/5 my-4 opacity-25" />

		<div class="text-2xl">"{data?.paperTitle}"</div>
		<div class="mt-2 text-base opacity-60 font-light">{data?.about}</div>
	</div>
</div>
