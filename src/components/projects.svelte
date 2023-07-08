<script lang="ts">
  import CardImage from "./cardImage.svelte";
  import CardText from "./cardText.svelte";
  import thefield from "$lib/images/thefield.png";
  import novaris from "$lib/images/novaris.png"
  let textClass = "text-white ";

  setTimeout(() => {
    textClass =
      "text-transparent bg-clip-text bg-gradient-to-r from-white to-orange-500 to-50%";
  }, 500);
</script>

<main class="px-8 py-5">
  <h1
    class="font-extrabold montserrat text-9xl text-center transition-all {textClass}"
  >
    FRONTEND
  </h1>
  <div class="min-h-screen w-full grid grid-cols-2 grid-flow-row gap-2 mt-10">
    <CardImage image={thefield} />
    <CardText
      title={"The field"}
      classprop={"first-letter:text-lime-600"}
      description={`This project is one of the best projects I've worked on. It's a social media app with a sports theme. The app is built using Next.js and MongoDB as the database, and it has a connection with a Golang backend. Additionally, it utilizes the Next.js API.`}
      githubLink={"https://github.com/alopez-2018459/the-field-app"}
      next={true}
      golang={true}
    />

    <CardText
      title={"Novaris"}
      classprop={"first-letter:text-purple-600"}
      description={`In this project, I worked with a small team to create a banking system app. The app utilizes Next.js Auth for authentication and the Next.js API as the backend. My role in this project was to lead the team, provide solutions, and supervise the team by conducting revisions.`}
      githubLink={"https://github.com/alopez-2018459/bank-app"}
      next={true}
      golang={false}
    />
    <CardImage image={novaris} />
  </div>
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@600&display=swap");

  .montserrat {
    font-family: "Montserrat", sans-serif;
  }
</style>
