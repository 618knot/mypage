<script>
  import knot from "$lib/assets/logo/knot.svg";
  import x from "$lib/assets/logo/x.svg";
  import github from "$lib/assets/logo/github-mark-white.svg";

  import code from "$lib/assets/icon/code.svg";
  import mapPin from "$lib/assets/icon/mappin.svg";
  import note from "$lib/assets/icon/note.svg";

  import ProfileLine from "$lib/components/ProfileLine.svelte";
  import BlogLinkCard from "$lib/components/BlogLinkCard.svelte";
</script>

<main class="text-gray-200 flex flex-col items-center gap-8 pt-9">
  <div class="flex flex-col items-center text-center gap-8">
    <img src={knot} alt="" />
    <div class="flex flex-col items-center gap-4">
      <div>
        <h1 class="text-3xl font-bold">のっと.</h1>
        <span class="text-xs font-medium text-gray-400">@618knot</span>
      </div>
    
      <div class="flex gap-8">
        <a href="https://x.com/618knot">
          <img src={x} alt="X link" class="hover:opacity-70 transition-opacity duration-300" />
        </a>
        <a href="https://github.com/618knot">
          <img src={github} alt="GitHub link" class="hover:opacity-70 transition-opacity duration-300" />
        </a>
      </div>
    </div>
  </div>

  <div class="space-y-2.5">
    <ProfileLine icon={mapPin} alt="location">Hokkaido</ProfileLine>
    <ProfileLine icon={code} alt="programming language">Ruby, Python, JavaScript, TypeScript</ProfileLine>
    <ProfileLine icon={note} alt="interested in">Web, Network, BLE</ProfileLine>
  </div>

  <div class="flex flex-col items-center space-y-4 w-full">
    <BlogLinkCard blogName="Zenn" account="@knot" url="https://zenn.dev/knot" />
    <BlogLinkCard blogName="Qiita" account="@knot" url="https://qiita.com/knot" />
    <BlogLinkCard blogName="note" account="@618knot" url="https://qiita.com/knot" />
  </div>
</main>
