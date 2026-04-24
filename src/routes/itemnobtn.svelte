<script>
    import Fancybtn from "./fancybtn.svelte";
    let props = $props();
</script>
<div class="rounded-lg bg-zinc-900 p-2 px-4 pr-2 text-zinc-100 text-lg border-t-1 border-zinc-600 f1">
    <h3 class="font-semibold">{props.name}</h3>
    <hr class="border-zinc-500 my-2">
    <p>{@html props.description}</p>
</div>