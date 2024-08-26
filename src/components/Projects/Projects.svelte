<script>
  import { cn } from "../../lib/utils/cn";
  import DirectionAwareHover from "../UI/DirectionAwareHover/DirectionAwareHover.svelte";
  import Button from "../UI/MovingBorder/Button.svelte";
  import ProjectCard from "./ProjectCard.svelte";

  export const Projects = [
    {
      title: "Ale Interior",
      techstack: [
        "mdi:react",
        "mdi:tailwind",
        "devicon-plain:sanity",
        "fa6-brands:sass",
      ],
      livelink: "https://aleinterior.com",
      cover: "/aleinterior.png",
      background: "bg-glowskyblue",
    },
    {
      title: "ES Ecommerce App",
      techstack: [
        "mdi:react",
        "simple-icons:express",
        "simple-icons:mongodb",
        "mdi:tailwind",
        "fa6-brands:sass",
      ],
      github: "https://github.com/ElnatanSamuel/Fullecom",
      livelink: "https://monel.vercel.app//",
      cover: "/ecomproj.png",
      background: "bg-slightpurple",
    },
    {
      title: "React",
      techstack: ["mdi:react", "mdi:react", "mdi:react", "mdi:react"],
      github: "https://github.com",
      livelink: "https://github.com",
      cover: "/portfolio.png",
      background: "bg-glowskyblue",
    },
    {
      title: "React",
      techstack: ["mdi:react", "mdi:react", "mdi:react", "mdi:react"],
      github: "https://github.com",
      livelink: "https://github.com",
      cover: "/portfolio.png",
      background: "bg-slightpurple",
    },
  ];
</script>

<div>
  <div class="py-10 mt-10 p-0 md:p-5 text-white">
    <div
      class="flex flex-col items-center justify-start mt-10 -rotate-6 text-white"
    >
      <h1
        class="items-start text-xl md:text-3xl cursor-pointer font-bold transition-all z-50"
      >
        Projects 🚀
      </h1>
      <div class="w-28 md:w-36 h-2 rounded-full bg-glowskyblue"></div>
      <div
        class="w-28 md:w-36 h-2 rounded-full bg-slightpurple translate-x-2"
      ></div>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-2 pt-20 gap-5">
      {#each Projects as project, idx}
        <div>
          <div class={cn("p-5 rounded-md ", project.background)}>
            <div class=" space-y-5 py-4 bg-black/[.4] pl-4 pr-20 rounded-md">
              <h1 class="text-2xl font-semibold">{project.title}</h1>
              <div class="flex item-center gap-5">
                {#each project.techstack as tech}
                  <iconify-icon icon={tech} width="30"></iconify-icon>
                {/each}
              </div>
              <div class="flex items-center gap-5">
                {#if project.github}
                  <a href={project.github} target="_blank"
                    ><Button borderRadius=".5rem" className="p-3"
                      ><p class=" font-semibold">🔗 GITHUB</p></Button
                    ></a
                  >{/if}
                {#if project.livelink}
                  <a href={project.livelink} target="_blank"
                    ><Button borderRadius=".5rem" className="p-3"
                      ><p class=" font-semibold">🌐 LIVE</p></Button
                    ></a
                  >{/if}
              </div>
            </div>
          </div>
          <div class="flex items-center justify-center mt-4 gap-5">
            <Button borderRadius=".5rem" className="p-3 block md:hidden"
              ><p class=" font-semibold">🔗 GITHUB</p></Button
            >
            <Button borderRadius=".5rem" className="p-3 block md:hidden"
              ><p class=" font-semibold">🌐 LIVE</p></Button
            >
          </div>
        </div>
      {/each}
    </div>
  </div>
</div>
