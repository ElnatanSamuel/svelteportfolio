<script>
  import { cn } from "../../lib/utils/cn";
  import DirectionAwareHover from "../UI/DirectionAwareHover/DirectionAwareHover.svelte";
  import Button from "../UI/MovingBorder/Button.svelte";
  import Projects from "./Projects.svelte";
</script>

<div class="grid grid-cols-1 sm:grid-cols-2 pt-20 gap-5">
  {#each Projects as project, idx}
    <div class={cn("p-5 rounded-md", project.background)}>
      <DirectionAwareHover
        imageUrl={project.cover}
        className="w-full  md:h-10  space-y-5 cursor-pointer"
      >
        <a href="." class="space-y-5 bg-black/[.3] py-4 px-10 rounded-md">
          <h1 class="text-2xl font-semibold">{project.title}</h1>
          <div class="flex item-center gap-5">
            {#each project.techstack as tech}
              <iconify-icon icon={tech} width="30"></iconify-icon>
            {/each}
          </div>
          <div class="flex items-center gap-5">
            <Button borderRadius=".5rem" className="p-3"
              ><p class=" font-semibold">🔗 GITHUB</p></Button
            >
            <Button borderRadius=".5rem" className="p-3"
              ><p class=" font-semibold">🌐 LIVE</p></Button
            >
          </div>
        </a>
      </DirectionAwareHover>
    </div>
  {/each}
</div>
