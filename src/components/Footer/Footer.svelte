<script>
  import {
    FilePdfOutline,
    GithubSolid,
    LinkedinSolid,
  } from "flowbite-svelte-icons";
  import Navbar from "../NavBar/Navbar.svelte";
</script>

<div class="border-t border-white/[.1] mt-10">
  <div
    class="text-white py-10 flex flex-col gap-5 justify-between items-center"
  >
    <h1
      class="text-2xl -rotate-2 font-bold underline underline-offset-8 z-20 decoration-glowskyblue"
    >
      E.S 👨🏻‍💻
    </h1>

    <div class="flex justify-center items-center space-x-4 z-20">
      <a href="https://www.linkedin.com/in/elnatansamuel999/" target="_blank"
        ><LinkedinSolid size="xl" class="cursor-pointer" /></a
      >
      <a href="https://github.com/ElnatanSamuel/" target="_blank"
        ><GithubSolid size="xl" class="cursor-pointer" /></a
      >
      <a href="/Elnatan-Samuel2024.pdf" target="_blank">
        <FilePdfOutline size="xl" class="cursor-pointer" />
      </a>
    </div>
  </div>
</div>
