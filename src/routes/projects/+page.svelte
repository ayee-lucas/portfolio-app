<script>
  import bg from "$lib/images/bgwebp.webp";
  import "animate.css";
  import Projects from "../../components/projects.svelte";
</script>

<main class="min-h-screen bg-black">
  <div class="w-full relative h-56">
    <div class="bg-black/40 z-[3] absolute inset-0" />
    <h1
      class="absolute tracking-[2px] transition-all text-white text-5xl left-5 top-1/2 z-[4] animate__animated animate__fadeInUp
      inter
    "
    >
      PROJECTS
    </h1>
    <img
      src={bg}
      alt="background"
      class="absolute w-full h-full object-cover z-[2]"
    />
  </div>
  <Projects />
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Inter:wght@600&display=swap");

  .inter {
    font-family: "Inter", sans-serif;
  }
</style>
