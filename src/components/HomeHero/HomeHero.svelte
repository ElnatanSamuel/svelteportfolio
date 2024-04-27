<script>
  import { onMount } from "svelte";
  import Button from "../UI/MovingBorder/Button.svelte";
  import { fly } from "svelte/transition";

  let animate = false;

  onMount(() => {
    animate = true;
  });
</script>

<div
  class="min-h-[80vh] gap-16 lg:gap-0 flex flex-col-reverse justify-between items-center text-white lg:flex-row"
>
  {#if animate}
    <div
      class="space-y-10 flex flex-col items-center lg:items-baseline pt-6 lg:pt-0"
    >
      <h1
        class="text-2xl md:text-4xl lg:text-7xl font-bold text-center lg:text-left"
        in:fly={{ y: 50, opacity: 0, duration: 500, delay: 50 }}
      >
        Hello! 👋 <br />
        <span class="underline underline-offset-8 decoration-glowskyblue"
          >I'm Elnatan Samuel.</span
        >
      </h1>
      <p
        class="text-sm md:text-lg text-gray-300 lg:w-[600px] text-center lg:text-left"
        in:fly={{ y: 50, opacity: 0, duration: 500, delay: 100 }}
      >
        I'm a Full Stack Web Developer and gaming aficionado ready to code your
        next epic quest. Let's level up your ideas into interactive, web-based
        adventures!
      </p>
      <div
        class="mb-20"
        in:fly={{ y: 100, opacity: 0, duration: 500, delay: 150 }}
      >
        <a href="mailto:elnatan23samuel@gmail.com"
          ><button
            class="inline-block z-20 text-xl md:text-3xl cursor-pointer font-bold hover:text-glowskyblue transition-all"
          >
            Contact Me 📪
          </button></a
        >
        <div class="w-36 md:w-40 h-2 rounded-full bg-glowskyblue"></div>
        <div
          class="w-36 md:w-40 h-2 rounded-full bg-slightpurple translate-x-2"
        ></div>
      </div>
    </div>
    <div class="opacity-1 relative pt-10 pl-10 md:pl-0 lg:pt-0">
      <div class="w-72 h-72 space-y-3 -rotate-[30deg]">
        <div class="flex gap-3 translate-x-8">
          <div
            class=" w-32 h-32 z-20 rounded-2xl bg-glowskyblue"
            in:fly={{ y: 100, opacity: 0, duration: 500, delay: 100 }}
          ></div>
          <div
            class=" w-32 h-32 z-20 rounded-full bg-slightpurple"
            in:fly={{ y: 100, opacity: 0, duration: 500, delay: 200 }}
          ></div>
        </div>
        <div class="flex gap-3 z-20 -translate-x-8">
          <div
            class=" w-32 h-32 z-20 rounded-2xl bg-slightpurple"
            in:fly={{ y: 100, opacity: 0, duration: 1000, delay: 300 }}
          ></div>
          <div
            class=" w-32 h-32 z-20 rounded-full bg-glowskyblue"
            in:fly={{ y: 100, opacity: 0, duration: 1000, delay: 400 }}
          ></div>
        </div>
        <div class="glow absolute top-[40%] right-1/2 -z-10"></div>
      </div>
      <div
        class="absolute bottom-5 sm:bottom-14 left-8 sm:-left-10"
        in:fly={{ opacity: 0, duration: 2000, delay: 1000 }}
      >
        <Button borderRadius=".5rem" className="p-3"
          ><p class=" font-semibold">📢 Available for work</p></Button
        >
      </div>
    </div>
  {/if}
</div>
