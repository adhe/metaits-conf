<script>
  export let id, date, description;
</script>

<div>
  <div class="flex flex-col items-center">
    <div class=" w-full xl:flex items-center justify-center hidden">
      <div class={`${id === '1' ? 'border-0' : 'border-t border-gray-300 '} flex-grow`}></div>
      <div class="rounded-full size-4 border-4 border-[#009EA8]"></div>
      <div class={`${id === '6' ? 'border-0' : 'border-t border-gray-300 '} flex-grow`}></div>
    </div>
    <div class="mt-5 xl:mb-2 font-semibold text-lg xl:text-[1.4rem] text-center">{date}</div>
    <div class="text-sm xl:text-base px-4 text-gray-500 text-center xl:leading-tight">
      {description}
    </div>
  </div>
</div>
