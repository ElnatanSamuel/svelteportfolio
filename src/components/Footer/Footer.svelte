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
      <LinkedinSolid size="xl" class="cursor-pointer" />
      <GithubSolid size="xl" class="cursor-pointer" />
      <FilePdfOutline size="xl" class="cursor-pointer" />
    </div>
  </div>
</div>
