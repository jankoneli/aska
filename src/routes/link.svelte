<!-- eslint-disable -->
<script>
    let props = $props();
</script>
<a href="{props.url}" class="w-full">
    <div class={["bg-red-800 border-t-2 duration-150 text-4xl flex justify-between hover:bg-red-900 border-red-600 p-8 rounded-lg text-zinc-100 w-full"]}>
        <h1 class="f1 text-4xl">{props.title}</h1>
        <i class="bi bi-arrow-right"></i>
    </div>
</a>