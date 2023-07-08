<script>
  import "animate.css";
  import Projects from "../../components/projects.svelte";
  import SmallProjects from "../../components/SmallProjects.svelte";
</script>

<main class="min-h-screen bg-black">
  <div class="w-full relative h-56 bg-gradient-to-r from-zinc-800 to-black">
    <div class="bg-black/40 z-[3] absolute inset-0" />
    <h1
      class="absolute tracking-[2px] transition-all text-white text-5xl left-5 top-1/2 z-[4] animate__animated animate__fadeInUp
      inter
    "
    >
      FEATURED PROJECTS
    </h1>

  </div>
  <Projects />
  <SmallProjects />
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Inter:wght@600&display=swap");

  .inter {
    font-family: "Inter", sans-serif;
  }
</style>
