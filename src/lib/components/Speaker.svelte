<script>
	export let data;
	</script>

<div class="xl:flex xl:space-x-8 py-8 xl:py-12">
	<div class="w-1/2 xl:w-1/4 mb-5 flex mx-auto">
		<img src={data?.photoUrl} class="w-full h-52 xl:h-72 object-cover rounded-md xl:rounded-2xl" alt="">
	</div>
	<div class="flex-1 text-white">
		<div class="text-xl text-center xl:text-left xl:text-3xl font-medium">{data?.name}</div>
		<div class="opacity-75 text-center xl:text-left xl:text-lg">{data?.university}</div>

		<div class="border-t w-1/5 my-4 opacity-25 mx-auto xl:mx-0" />

		<div class="text-lg xl:text-2xl leading-tight">"{data?.paperTitle}"</div>
		<div class="mt-2 text-base opacity-60 font-light">{data?.about}</div>
	</div>
</div>
