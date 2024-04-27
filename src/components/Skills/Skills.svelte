<script>
  import { ReactSolid } from "flowbite-svelte-icons";
  import CardHoverEffect from "../UI/CardHoverEffect/CardHoverEffect.svelte";

  const proj = [
    {
      title: "React",
      Icon: "mdi:react",
    },
    {
      title: "Svelte",
      Icon: "ri:svelte-fill",
    },
    {
      title: "Tailwind CSS",
      Icon: "mdi:tailwind",
    },
    {
      title: "NodeJS",
      Icon: "akar-icons:node-fill",
    },
    {
      title: "Express JS",
      Icon: "simple-icons:express",
    },
    {
      title: "MongoDB",
      Icon: "bxl:mongodb",
    },
    {
      title: "React Native",
      Icon: "tabler:brand-react-native",
    },
    {
      title: "Git",
      Icon: "mdi:git",
    },
  ];
</script>

<div class="mt-28 md:mt-16 text-white max-w-5xl m-auto px-2">
  <div class="flex flex-col items-center justify-start rotate-6">
    <h1
      class="items-start z-20 text-xl md:text-3xl cursor-pointer font-bold transition-all"
    >
      Skills 🛠️
    </h1>
    <div class="w-28 md:w-36 h-2 rounded-full bg-glowskyblue"></div>
    <div
      class="w-28 md:w-36 h-2 rounded-full bg-slightpurple translate-x-2"
    ></div>
  </div>

  <CardHoverEffect items={proj} />
</div>
