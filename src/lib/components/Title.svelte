<script>
  export let title;
</script>

<div id={title} class="container mx-auto pt-16 xl:pt-28 flex flex-col items-center">
  <div class="w-4/5 flex items-center space-x-6">
    <div class="grow border-t-2 w-20" />
    <div class="text-2xl text-center xl:text-4xl font-semibold xl:font-medium text-gradient-meta">
      {title}
    </div>
    <div class="grow border-t-2 w-20" />
  </div>
</div>
