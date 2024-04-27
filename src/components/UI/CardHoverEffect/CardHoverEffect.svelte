<script>
  import { Motion, AnimatePresence } from "svelte-motion";
  import { cn } from "../../../lib/utils/cn";
  export let items = [{ title, Icon }];
  export let className = undefined;
  let Icons = null;
  let hoveredIndex = null;
</script>

<div class={cn("grid  py-10  grid-cols-2  lg:grid-cols-3", className)}>
  {#each items as item, idx}
    <div
      href="./"
      key={item.title}
      class="group relative block h-full w-full p-2"
      on:mouseenter={() => (hoveredIndex = idx)}
      on:mouseleave={() => (hoveredIndex = null)}
    >
      <AnimatePresence show={true}>
        {#if hoveredIndex === idx}
          <Motion
            let:motion
            layoutId="hoverBackground"
            initial={{ opacity: 0 }}
            animate={{
              opacity: 1,
              transition: { duration: 0.15 },
            }}
            exit={{
              opacity: 0,
              transition: { duration: 0.5, delay: 0.5 },
            }}
          >
            <span
              use:motion
              class="absolute inset-0 h-full w-full rounded-lg bg-slightpurple dark:black/[0.8]"
            />
          </Motion>
        {/if}
      </AnimatePresence>
      <div
        class={cn(
          "rounded-md w-full p-4 overflow-hidden bg-black group-hover:ring-2 ring-glowskyblue relative z-20 transition-all duration-500 cursor-pointer",
          className
        )}
      >
        <div class="relative z-50 cursor-pointer">
          <div
            class="py-5 md:py-10 z-50 relative space-y-5 flex flex-col items-center"
          >
            <h4
              class={cn(
                "mt-4 font-bold tracking-wide text-zinc-100",
                className
              )}
            >
              <iconify-icon icon={item.Icon} width="30"></iconify-icon>
            </h4>
            <p
              class={cn(
                " text-lg md:text-2xl font-semibold text-center text-gray-300",
                className
              )}
            >
              {item.title}
            </p>
          </div>
        </div>
      </div>
    </div>
  {/each}
</div>
