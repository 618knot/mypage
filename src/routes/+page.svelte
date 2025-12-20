<script>
  import knot from "$lib/assets/logo/knot.svg";
  import x from "$lib/assets/logo/x.svg";
  import github from "$lib/assets/logo/github-mark-white.svg";

  import code from "$lib/assets/icon/code.svg";
  import mapPin from "$lib/assets/icon/mappin.svg";
  import note from "$lib/assets/icon/note.svg";

  import ProfileLine from "$lib/components/ProfileLine.svelte";
  import BlogLinkCard from "$lib/components/BlogLinkCard.svelte";
	import ProfileTab from "$lib/parts/ProfileTab.svelte";
</script>

<main class="text-gray-200 flex flex-col items-center gap-8 pt-9 flex-1 w-full min-h-0">
  <div class="flex flex-col items-center text-center gap-6">
    <img src={knot} alt="" />
    <div class="flex flex-col items-center gap-4">
      <div>
        <h1 class="text-3xl font-bold">のっと.</h1>
        <span class="text-xs font-medium text-gray-400">@618knot</span>
      </div>
    
      <div class="flex gap-8">
        <a href="https://x.com/618knot" target="_blank" rel="noreferrer">
          <img src={x} alt="X link" class="hover:opacity-70 transition-opacity duration-300" />
        </a>
        <a href="https://github.com/618knot" target="_blank" rel="noreferrer">
          <img src={github} alt="GitHub link" class="hover:opacity-70 transition-opacity duration-300" />
        </a>
      </div>
    </div>
  </div>

  <div class="space-y-2">
    <ProfileLine icon={mapPin} alt="location">Hokkaido</ProfileLine>
    <ProfileLine icon={code} alt="programming language">Ruby, JavaScript, TypeScript</ProfileLine>
    <ProfileLine icon={note} alt="interested in">Web</ProfileLine>
  </div>

  <ProfileTab />
</main>
