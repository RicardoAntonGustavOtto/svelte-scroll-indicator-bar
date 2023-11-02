<script>
    let scrolledValue = 0;

    $: clientHeight = 0;
    $: innerHeight = 0;
</script>

<div class="h-[3000px] bg-black"  bind:clientHeight>
    <div class="fixed bg-red-500 h-3" style="width: {scrolledValue/(clientHeight-innerHeight)*100}%;"></div>
</div>
<footer class="h-10 bg-green-500">

</footer>

<svelte:window bind:scrollY={scrolledValue} bind:innerHeight />