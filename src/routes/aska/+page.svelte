<style>
    @import url('https://fonts.googleapis.com/css2?family=Atkinson+Hyperlegible:ital,wght@0,400;0,700;1,400;1,700&family=Cormorant:ital,wght@0,300..700;1,300..700&family=Instrument+Serif:ital@0;1&family=Neuton:ital,wght@0,200;0,300;0,400;0,700;0,800;1,400&display=swap');
    @import "tailwindcss";
    .f1 {
        font-family: Cormorant, sans-serif;
    }
    .f2 {
        font-family: "Atkinson Hyperlegible", sans-serif;
    }
</style>
<script>
    let downloads = {
        "English":[
            {
                "url":"/english-aska.pdf",
                "desc":"Download English ASKA Material (.pdf)"
            }
        ],
        "Matematika":[
            {
                "url":"/matematika-bahas-assgp.pptx",
                "desc":"Download Pembahasan ASSGp Matematika (.pptx)"
            }
        ]
    }
</script>
<main>
    <div class="w-full p-8 bg-blue-800 border-b-2 border-blue-600">
        <a href="/" class="hover:bg-zinc-300 duration-150 bg-zinc-100 border-b-2 border-zinc-300 rounded-lg outline-none decoration-0 p-2 px-3 f1 font-bold text-xl"><i class="bi bi-arrow-left"></i> Return to Main</a>
        <h1 class="f1 text-5xl font-bold text-center text-zinc-100 mt-12">Materi ASKA</h1>
        <p class="text-center font-normal text-zinc-100/70 mt-6 mb-6 text-xl f2">Materi untuk Asesmen Sumatif Kelas Akhir</p>
    </div>
    <div class="lg:p-24 p-12">
        {#each Object.keys(downloads) as file}
            <h1 class="text-4xl f1 font-bold text-zinc-100">{file}</h1>
            <div class="pt-4 text-blue-400 f2 text-xl mb-12">
            {#each downloads[file] as url}
                <a href="{url.url}" class="hover:text-blue-500 duration-150">{url.desc}</a>
            {/each}
            </div>
        {/each}
    </div>
</main>