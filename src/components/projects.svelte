<script lang="ts">
  import CardImage from "./cardImage.svelte";
  import CardText from "./cardText.svelte";
</script>

<main class="px-5 py-5">
  <h1
    class="font-extrabold text-transparent text-4xl bg-clip-text bg-gradient-to-r from-white to-orange-500 to-15% montserrat"
  >
    FRONTEND
  </h1>
  <div class="min-h-screen w-full grid grid-cols-2 grid-flow-row gap-2 mt-10">
    <CardImage />
    <CardText
      title={"The field"}
      classprop={"first-letter:text-lime-600"}
      description={`This project is one of the best projects I've worked on. It's a social media app with a sports theme. The app is built using Next.js and MongoDB as the database, and it has a connection with a Golang backend. Additionally, it utilizes the Next.js API.`}
    />
  </div>
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@600&display=swap");

  .montserrat {
    font-family: "Montserrat", sans-serif;
  }
</style>
