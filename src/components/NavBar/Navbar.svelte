<script>
  import {
    LinkedinSolid,
    GithubSolid,
    FilePdfOutline,
  } from "flowbite-svelte-icons";
</script>

<nav class="text-white py-10 flex justify-between items-center">
  <h1
    class="text-2xl -rotate-2 font-bold underline underline-offset-8 z-20 decoration-glowskyblue"
  >
    E.S 👨🏻‍💻
  </h1>

  <div class="flex justify-center items-center space-x-4 z-20">
    <a
      href="https://www.linkedin.com/in/elnatan-samuel-3bb266286/"
      target="_blank"><LinkedinSolid size="xl" class="cursor-pointer" /></a
    >
    <a href="https://github.com/ElnatanSamuel/" target="_blank"
      ><GithubSolid size="xl" class="cursor-pointer" /></a
    >
    <FilePdfOutline size="xl" class="cursor-pointer" />
  </div>
</nav>
