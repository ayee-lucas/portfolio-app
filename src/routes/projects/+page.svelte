<script>
  import bg from "$lib/images/bgwebp.webp";
  import "animate.css";
  import Projects from "../../components/projects.svelte";

  let textClass = "";

  setTimeout(() => {
    textClass = "bg-clip-text text-transparent bg-gradient-to-r from-white to-zinc-500";
  }, 1000);
</script>

<main class="min-h-screen bg-black">
  <div class="w-full relative h-56">
    <div class="bg-black/40 z-[3] absolute inset-0" />
    <h1
      class="absolute transition-all text-white text-5xl left-32 top-1/2 z-[4] animate__animated animate__fadeInUp
      {textClass}
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
