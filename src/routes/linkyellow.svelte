<script>
    let props = $props();
</script>
<a href="{props.url}" class="w-full">
    <div class={["bg-yellow-800 border-t-2 lg:h-48 duration-150 text-4xl flex justify-between hover:bg-yellow-900 border-yellow-600 p-8 rounded-lg text-zinc-100 w-full"]}>
        <h1 class="f1 text-4xl">{props.title}</h1>
        <i class="bi bi-arrow-right"></i>
    </div>
</a>