<script lang="ts">
	import BlogLinkCard from "$lib/components/BlogLinkCard.svelte";
  import { fade } from "svelte/transition";
  import clsx from "clsx";
	import EventLinkCard from "$lib/components/EventLinkCard.svelte";

  let activeTab = $state("blogs");

  const tabs = [
    { id: "blogs", name: "Blog" },
    { id: "event", name: "Conference" },
  ];
</script>

<div class="w-full flex flex-col flex-1 min-h-0">
  <div class="mx-auto w-fit mb-4 space-x-1">
    {#each tabs as tab}
      <button
        class={clsx("px-4 py-2 transition-colors duration-200 text-gray-200", {
          "border-b-2 border-gray-50 border-opacity-50": activeTab === tab.id,
          "text-opacity-50 hover:text-opacity-100": activeTab !== tab.id,
        })}
        onclick={() => (activeTab = tab.id)}
      >
        {tab.name}
      </button>
    {/each}
  </div>

  <div class="flex flex-col items-center space-y-4 w-full flex-1 overflow-y-auto pb-4 no-scrollbar">
    {#if activeTab === "blogs"}
      <BlogLinkCard blogName="Zenn" account="@knot" url="https://zenn.dev/knot" />
      <BlogLinkCard blogName="Qiita" account="@knot" url="https://qiita.com/knot" />
      <BlogLinkCard blogName="note" account="@618knot" url="https://note.com/618knot/" />
    {/if}
    {#if activeTab === "event"}
      <EventLinkCard name="フロントエンドカンファレンス北海道2025" date="2025.09.06" url="https://fortee.jp/frontend-conf-hokkaido-2025" role="コアスタッフ" />
      <EventLinkCard name="フロントエンドカンファレンス北海道2024" date="2024.08.24" url="https://fortee.jp/frontend-conf-hokkaido-2024" role="コアスタッフ" />
      <EventLinkCard name="TechRAMEN 2024 Conference" date="2023.08.26" url="https://fortee.jp/techramen-24-conf" role="一般参加" />
      <EventLinkCard name="PHPカンファレンス北海道2024" date="2024.01.13" url="https://fortee.jp/phpcon-hokkaido-2024" role="当日スタッフ" />
    {/if}
  </div>
</div>
