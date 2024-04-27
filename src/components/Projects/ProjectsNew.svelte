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
      techstackword: ["React", "Tailwindcss", "Sanity", "Sass"],
      livelink: "https://aleinterior.com",
      cover: "/aleinterior.png",
      background: "bg-glowskyblue",
      desc: " Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sapiente ex perferendis dolor quos laborum illum nam dicta, temporibus eligendi. Ex!",
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
      techstackword: ["React", "Tailwindcss", "Express", "MongoDB", "Sass"],
      github: "https://github.com/ElnatanSamuel/Fullecom",
      livelink: "https://full.ecom.elnatansamueldev.com/",
      cover: "/ecomproj.png",
      background: "bg-slightpurple",
      desc: " Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sapiente ex perferendis dolor quos laborum illum nam dicta, temporibus eligendi. Ex!",
    },
    {
      title: "React",
      techstack: ["mdi:react", "mdi:react", "mdi:react", "mdi:react"],
      techstackword: ["React", "Tailwindcss", "Sanity", "Sass"],
      github: "https://github.com",
      livelink: "https://github.com",
      cover: "/portfolio.png",
      background: "bg-glowskyblue",
      desc: " Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sapiente ex perferendis dolor quos laborum illum nam dicta, temporibus eligendi. Ex!",
    },
    {
      title: "React",
      techstack: ["mdi:react", "mdi:react", "mdi:react", "mdi:react"],
      techstackword: ["React", "Tailwindcss", "Sanity", "Sass"],
      github: "https://github.com",
      livelink: "https://github.com",
      cover: "/portfolio.png",
      background: "bg-slightpurple",
      desc: " Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sapiente ex perferendis dolor quos laborum illum nam dicta, temporibus eligendi. Ex!",
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

    <div class="projectcontainer">
      {#each Projects as project, idx}
        <div class="projectcard rounded-lg">
          <img class="w-full h-full object-fit" src={project.cover} alt="" />
          <div class="text-center w-full">
            <p class="font-bold text-glowskyblue pt-4 pb-2 text-xl md:text-2xl">
              {project.title}
            </p>
            <div class="w-[50px] h-1 mx-auto my-2 bg-glowskyblue"></div>
          </div>
          <p
            class="w-full text-gray-200 text-sm md:text-lg text-justify leading-6 p-4"
          >
            {project.desc}
          </p>
          <div>
            <p
              class="text-center z-20 text-glowskyblue w-full mt-[10px] font-bold text-sm md:text-lg"
            >
              Tech Stack
            </p>
            <div class="flex flex-wrap justify-center items-center gap-6 p-2">
              {#each project.techstackword as tech}
                <!-- <iconify-icon icon={tech} width="30"></iconify-icon> -->
                <p class="text-white font-bold text-xs md:text-md">
                  {tech}
                </p>
              {/each}
            </div>
            <div class="flex justify-center items-center space-x-16 my-6">
              {#if project.github}
                <a href={project.github} target="_blank"
                  ><Button borderRadius=".5rem" className="p-2"
                    ><p class=" font-semibold">🔗 GITHUB</p></Button
                  ></a
                >{/if}
              {#if project.livelink}
                <a href={project.livelink} target="_blank"
                  ><Button borderRadius=".5rem" className="p-2"
                    ><p class=" font-semibold">🌐 LIVE</p></Button
                  ></a
                >{/if}
            </div>
          </div>
        </div>
      {/each}
    </div>
  </div>
</div>
