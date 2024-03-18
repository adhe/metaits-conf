<script>
	import { Topics, Speakers } from '../lib/data.js';
	import TopicItem from '$lib/components/TopicItem.svelte';
	import Speaker from '$lib/components/Speaker.svelte';
	import ArrowDown from '$lib/assets/ArrowDown.svelte';
</script>

<div class=" min-h-screen font-medium w-full flex">
	<div
		class="bg-gradient-to-tr from-[#003844] to-[#009EA8] text-white px-24 py-3 flex flex-col justify-between w-3/5"
	>
		<div class="py-6">
			<img src="metaits-logo-white.svg" class="h-12" alt="" />
		</div>
		<div>
			<div class=" text-3xl font-medium border-2 border-white px-5 py-2 rounded-full inline-block">
				Call for paper
			</div>
			<div class="mt-6 text-6xl font-semibold">
				1st Medical Technology and Applications International Conference 2024
			</div>
		</div>
		<div class="flex items-center justify-between border-t border-white/35 pt-8 pb-12">
			<div>
				<div class="text-3xl font-light">
					<span class="font-bold">10-12</span> October 2024
				</div>
				<div class="text-xl font-light">JW Marriot Hotel Surabaya</div>
				<div class=" font-light tracking-wider underline opacity-80">See important dates</div>
			</div>
			<div>
				<button class="bg-white rounded-full px-8 py-4 text-xl text-teal-950 flex items-center">
					More Info
					<div class="size-6 rounded-full ml-5">
						<ArrowDown />
					</div>
				</button>
			</div>
		</div>
	</div>
	<div class="bg-[#106476] w-2/5">
		<img src="foto-gedung-fkk-min.jpg" class="h-full object-cover" alt="" />
	</div>
</div>

<div class="container mx-auto py-32 flex flex-col items-center">
	<div class="text-5xl font-medium max-w-4xl text-center">
		“Collaborative Innovation: A Bridging from Academia to Industry towards Sustainable Strategic
		Partnership”
	</div>
	<div class="max-w-4xl text-center mt-12 text-lg text-gray-600">
		ISITIA 2024 is the annual international conference held by the Department of Electrical
		Engineering of the Institut Teknologi Sepuluh Nopember (ITS), Surabaya, Indonesia. It was
		previously known as SITIA and has been held annually by the department since 1999. This year,
		ISITIA will be held in hybrid.
	</div>
	<div class="max-w-4xl text-center mt-5 text-lg text-gray-600">
		Papers that are accepted and presented at ISITIA 2024 will be submitted for possible inclusion
		in IEEE Xplore, subject to meeting IEEE Xplore’s scope and quality requirements. If an author
		fails to register for the conference or does not present their paper, the paper will be flagged
		as a ‘no show’ and removed from the conference proceedings.
	</div>

	<div class="w-4/5 flex items-center space-x-6 mt-20">
		<div class="grow border-t-2 w-20" />
		<div class="relative text-5xl font-medium">
			Topics of interest
			<div class="absolute text-base opacity-50 bottom-0 translate-y-full inset-x-0 text-center">
				include, but are not limited to
			</div>
		</div>
		<div class="grow border-t-2 w-20" />
	</div>
	<div class="mt-12 grid grid-cols-3 gap-5">
		{#each Topics as topic}
			<TopicItem data={topic} />
		{/each}
	</div>
</div>

<div class="min-h-screen bg-teal-950">
	<div class="w-3/5 mx-auto py-32">
		<div class="text-5xl font-medium text-white text-center">Keynote Speaker</div>
		<div class="divide-y divide-white/25">
			{#each Speakers as speaker}
				<Speaker data={speaker} />
			{/each}
		</div>
	</div>
</div>