<script>
    import ListRepository from "./ListRepository.svelte";
    export let data = [
        {
            title:
                "Pengaruh Intervensi Cookies Galohgor Pada Ibu Postpartum Terhadap Tingkat Kecukupan dan Status Gizi Bayi ﻿",
            author_name: ["Nuraelah, Almira", "Roosita, Katrin "],
            short_dec:
                "Pemberian ASI merupakan salah satu cara paling efektif untuk meningkatkan kesehatan dan kelangsungan hidup anak. ASI merupakan makanan terbaik dan mengandung semua zat gizi yang dibutuhkan bayi dalam jumlah yang tepat ...",
            published_date: "2020",
            href: "google.com",
        },
        {
            title: "NOVEL",
            author_name: ["Indra", "tegar"],
            short_dec: "cek",
            published_date: "2020",
            href: "google.com",
        },
    ];
    export let is_odd = true;
</script>

<ul class="ds-artifact-list list-unstyled">
    {#each data as item, i}
        <ListRepository
            title={item.title}
            author_name={item.author_name}
            short_desc={item.short_dec}
            published_date={item.published_date}
            href={item.href}
            is_odd={i % 2 === 0} />
    {/each}
</ul>
