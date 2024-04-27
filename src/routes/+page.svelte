<script>
  import Footer from "../components/Footer/Footer.svelte";
  import HomeHero from "../components/HomeHero/HomeHero.svelte";
  import Navbar from "../components/NavBar/Navbar.svelte";
  import Projects from "../components/Projects/Projects.svelte";
  import Skills from "../components/Skills/Skills.svelte";
  import DotBackground from "../components/UI/GridBackground/DotBackground.svelte";
  import { quintOut } from "svelte/easing";
  import { onMount } from "svelte";
  import ProjectsNew from "../components/Projects/ProjectsNew.svelte";
</script>

<div class=" min-h-screen">
  <!-- <div class="bglinesthing"></div> -->
  <!-- <BackgroundBoxes2 className=" hidden lg:block" /> -->

  <DotBackground className="z-0">
    <div class="relative overflow-hidden">
      <div class="max-w-7xl m-auto px-6 z-10">
        <Navbar />
        <HomeHero />
      </div>

      <div
        class="h-10 xl:h-32 bg-gradient-to-t from-black absolute -bottom-8 left-0 xl:-bottom-18 w-full z-10"
      ></div>
    </div>
  </DotBackground>

  <div class="max-w-7xl m-auto px-2 md:px-6">
    <ProjectsNew />
    <Skills />
    <Footer />
  </div>
</div>
