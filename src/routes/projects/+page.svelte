<script>
  import "animate.css";
  import Projects from "../../components/projects.svelte";
  import SmallProjects from "../../components/SmallProjects.svelte";
  let headerClass = "bg-black"

  setTimeout(() => {

  headerClass = "bg-gradient-to-tr from-black via-black via-50% to-blue-500/30"

  },500)
  
</script>

<main class="min-h-screen bg-black">
  <div class="w-full relative h-56 transition-all {headerClass}">
    <div class="bg-black/40 z-[3] absolute inset-0" />
    <h1
      class="absolute tracking-[2px] transition-all text-white text-5xl left-5 top-1/2 z-[4] animate__animated animate__fadeInUp
      poppins font-light 
    "
    >
      Experience
    </h1>

  </div>
  <Projects />
  <SmallProjects />
</main>

<style>

  @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@200;600&display=swap");
  .poppins {
    font-family: "Poppins", sans-serif;
  }
</style>
