/* eslint-disable svelte/no-navigation-without-resolve */
<style>
    @import url('https://fonts.googleapis.com/css2?family=Atkinson+Hyperlegible:ital,wght@0,400;0,700;1,400;1,700&family=Cormorant:ital,wght@0,300..700;1,300..700&family=Instrument+Serif:ital@0;1&family=Neuton:ital,wght@0,200;0,300;0,400;0,700;0,800;1,400&display=swap');
    @import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.13.1/font/bootstrap-icons.min.css");
    *{
        font-family: "Atkinson Hyperlegible";
    }
    .f1 {
        font-family: "Cormorant";
    }
</style>
<script>
    import { Star } from "svelte-bootstrap-icons";
    import Fancybtn from "./fancybtn.svelte";
    import Link from "./link.svelte";
	import Item from "./item.svelte";
	import Itemnobtn from "./itemnobtn.svelte";
	import Linkblue from "./linkblue.svelte";
	import Linkyellow from "./linkyellow.svelte";
    let description = {
        "fisika":'<h2 id="kelas-7" class="font-bold text-zinc-500">Kelas 7</h2><p>Pengukuran</p><p>Sifat materi</p><p>Suhu dan penguraian</p><p>Kalor</p><p>Tatasurya</p><h2 id="kelas-8" class="font-bold text-zinc-500">Kelas 8</h2><p>Berat</p><p>Gaya dan hukum newton</p><p>Pesawat sederhana</p><p>Tekanan</p><p>Getaran dan gelombang</p><p>Cahaya</p><h2 id="kelas-9-" class="font-bold text-zinc-500">Kelas 9:</h2><p>Struktur atom</p><p>Listrik statis</p><p>Listrik dinamis</p><p>Kemagnetan</p>'
    }
    const agenda = [
        {
            tanggal: "Kamis, 30 April 2026",
            sesi: [
            { jam: "07.30-09.30", mapel: "B. Sunda", pg: 40, uraian: 5 }
            ]
        },
        {
            tanggal: "Senin, 4 Mei 2026",
            sesi: [
            { jam: "07.30-09.30", mapel: "IPA", pg: 40, uraian: 5 },
            { jam: "10.15-12.15", mapel: "PAK", pg: 40, uraian: 5 }
            ]
        },
        {
            tanggal: "Selasa, 5 Mei 2026",
            sesi: [
            { jam: "07.30-09.30", mapel: "B. Indonesia", pg: 35, uraian: 0 },
            { jam: "10.15-12.15", mapel: "PPKn", pg: 40, uraian: 5 }
            ]
        },
        {
            tanggal: "Rabu, 6 Mei 2026",
            sesi: [
            { jam: "07.30-09.30", mapel: "B. Inggris", pg: 40, uraian: 5 },
            { jam: "10.15-12.15", mapel: "PJOK", pg: 40, uraian: 5 }
            ]
        },
        {
            tanggal: "Kamis, 7 Mei 2026",
            sesi: [
            { jam: "07.30-09.30", mapel: "Informatika", pg: 40, uraian: 5 },
            { jam: "10.15-12.15", mapel: "B. Asing", pg: 40, uraian: 5 }
            ]
        },
        {
            tanggal: "Jumat, 8 Mei 2026",
            sesi: [
            { jam: "07.30-09.30", mapel: "IPS", pg: 40, uraian: 5 },
            { jam: "10.15-12.15", mapel: "Prakarya", pg: 40, uraian: 5 }
            ]
        },
        {
            tanggal: "Senin, 11 Mei 2026",
            sesi: [
            { jam: "07.30-09.30", mapel: "Matematika", pg: 30, uraian: 5 },
            { jam: "10.15-12.15", mapel: "Seni Budaya", pg: 40, uraian: 5 }
            ]
        }
    ];
</script>
<main class="duration-200">
    <!--Introduction-->
    <div class="lg:mt-80 mt-50 mb-12 justify-center flex flex-col gap-3">
        <h1 class="text-sky-100 text-center text-6xl lg:mx-0 mx-8 text-wrap lg:text-8xl f1 font-semibold">ASKA Resources</h1>
        <p class="text-sky-50/90 text-center lg:text-2xl font-regular mx-4">Apa itu ASKA? ASKA adalah singkatan dari <i>Asesmen Sumatif Kelas Akhir.</i> Website ini berisi materi atau kertas untuk latihan ASKA.</p>
        <!--div class="flex justify-center mt-4 gap-8 lg:flex-row flex-col mx-4 items-center">
            <input type="text" class="rounded-lg border-t-2 border-zinc-500 bg-zinc-800 outline-none text-2xl p-2 text-zinc-300 px-4 lg:w-6/12 duration-200 hover:w-7/12">
            <a href="/" class="rounded-lg bg-blue-600 text-left p-2 px-3 text-zinc-100 f1 font-semibold text-xl hover:bg-blue-700 duration-200 cursor-pointer border-t-1 border-blue-400"><i class="bi bi-asterisk"></i> Browse</a>
        </div-->
    </div>
    <hr class="border-zinc-600 mx-12">
    <!--Tryout Internal-->
    <!--Tryout Penabur-->
    <!--ASSGp-->
    <div class="lg:p-16 lg:px-24 p-12 f1 font-bold flex justify-between gap-8 lg:flex-row flex-col">
        <Link url="/assgp" title="Asesmen Sumatif Semester Genap 2026"/>
        <Linkblue url="/aska" title="Materi ASKA 2026"/>
        <Linkyellow url="/praktik" title="ASKA Praktik"/>
    </div>
    <div class="bg-zinc-800 p-8 lg:p-20 text-zinc-100 border-t-2 border-zinc-600">
        <h1 class="f1 text-5xl font-semibold"><i class="bi bi-caret-right-fill"></i> Agenda ASKA</h1>
        <p class="f1 mt-4 text-xl lg:text-2xl opacity-50">Asesmen Sumatif Kelas Akhir</p>
        <div class="flex flex-col gap-2 mt-6">
            {#each agenda as item}
                <div class="bg-zinc-900 p-4 rounded-lg border-t-2 border-zinc-700">
                    <h3 class="text-3xl font-bold f1 text-yellow-400 mb-2">{item.tanggal}</h3>
                    {#each item.sesi as sesi}
                        <p class="lg:text-xl text-md font-bold text-zinc-500">{sesi.jam} <span class="font-normal text-zinc-100">{sesi.mapel}</span> <span class="text-yellow-500/50">{sesi.pg} PG + {sesi.uraian} ESSAY</span></p>
                    {/each}
                </div>
            {/each}
        </div>
    </div>
</main>
