<script>
    let props = $props();
</script>
<div class="rounded-lg bg-zinc-900 p-2 px-4 pr-2 text-zinc-100 text-lg border-t-1 border-zinc-600 f1 flex justify-between items-center gap-1">
    <h3 class="font-semibold">{props.name}</h3>
    <div class="py-1">
        <a href={props.url} class="rounded-md bg-{props.color}-600 p-1 px-3 font-semibold text-xl text-nowrap hover:bg-{props.color}-700 border-t-1 border-{props.color}-400 cursor-pointer duration-200 font-semibold"><i class="bi bi-file-earmark-arrow-down-fill"></i> Download</a>
    </div>
</div>