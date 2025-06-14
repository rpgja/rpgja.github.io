<script>
    import { ExternalLinkIcon } from "@lucide/svelte";

    // サイトデータ（今後増やせる）
    const sites = [
        {
            title: "RPGEN非公式ウィキ",
            description: "RPGジェネレーター『RPGEN』の非公式ウィキです。",
            url: "https://rpgen.memo.wiki/",
            favicon:
                "https://image01.seesaawiki.jp/r/o/rpgen-memo/4863955a7ab17e06b1d8.png",
        },
        {
            title: "RPGENマップエディタ「ENRPG」",
            description: "RPGEN専用のマップエディタです。",
            url: "https://rpgja.github.io/enrpg/",
            favicon: null,
        },
        {
            title: "HGペイント（歩行グラフィックペイント）",
            description: "歩行グラを作れるフリーソフトです。",
            url: "https://rpgja.github.io/rpgen-walk/",
            favicon: "https://rpgja.github.io/rpgen-walk/midori.png",
        },
        {
            title: "VNメモ帳（ビジュアルノベルメモ帳）",
            description: "RPGENでビジュアルノベルを作る試み",
            url: "https://rpgja.github.io/rpgen-novel/",
            favicon: "https://rpgja.github.io/rpgen-novel/momoi.png",
        },
    ];

    const alternativeImg = "https://avatars.githubusercontent.com/u/170247206";
</script>

<section class="max-w-3xl mx-auto p-4 space-y-4">
    <h2 class="text-2xl font-bold mb-6">RPGEN非公式サイト一覧</h2>
    <p class="opacity-60">あなたのマップ制作を応援するサイトです。</p>
    <ul class="space-y-4">
        {#each sites as site}
            <li
                class="relative p-6 rounded-lg shadow hover:shadow-lg transition bg-base-200 overflow-hidden min-h-[6rem]"
            >
                <img
                    src={site.favicon ?? alternativeImg}
                    alt=""
                    aria-hidden="true"
                    class="pointer-events-none absolute right-0 -top-20 h-[16rem] w-auto opacity-20 select-none object-contain"
                />
                <div class="relative z-10">
                    <a
                        href={site.url}
                        target="_blank"
                        rel="noopener noreferrer"
                        class="font-semibold text-primary hover:underline flex items-center gap-1"
                    >
                        {site.title}
                        <ExternalLinkIcon class="inline-block w-4 h-4" />
                    </a>
                    <p class="text-sm text-base-content/70 mt-1 opacity-60">
                        {site.description}
                    </p>
                </div>
            </li>
        {/each}
    </ul>
</section>
