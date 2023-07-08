<script lang="ts">
  import CardImage from "./cardImage.svelte";
  import CardText from "./cardText.svelte";
  import thefield from "$lib/images/thefield.png";
  import novaris from "$lib/images/novaris.png";
  import Icon from "@iconify/svelte";
  let textClass = "text-white ";

  setTimeout(() => {
    textClass =
      "text-transparent bg-clip-text bg-gradient-to-r from-white to-blue-500 to-50%";
  }, 500);
</script>

<main class="px-8 py-5">
  <h1
    class=" montserrat text-9xl max-sm:text-4xl text-center transition-all pb-14 {textClass}"
  >
    FRONTEND
  </h1>
  <div
    class="min-h-screen w-full grid grid-cols-2 max-sm:grid-cols-1 grid-flow-row gap-2 mt-10 relative"
  >
    <CardImage image={thefield} />
    <CardText
      title={"The field"}
      classprop={"first-letter:text-lime-600"}
      description={`This project is one of the best projects I've worked on. It's a social media app with a sports theme. The app is built using Next.js and MongoDB as the database, and it has a connection with a Golang backend. Additionally, it utilizes the Next.js API.`}
      githubLink={"https://github.com/alopez-2018459/the-field-app"}
      next
      golang
      typescript
      mongo
    />
    <div
      class="absolute top-1/3 -left-52 w-96 h-96 rounded-full bg-gradient-to-r from-zinc-950 from-30% via-indigo-800  to-violet-900 animate-[spin_20s_linear_infinite]"
    />

    <div
      class="absolute top-1/3 -right-20 w-72 h-72 rounded-full bg-gradient-to-r from-green-800  via-lime-800 to-80%  to-black"
    />

    <CardText
      title={"Novaris"}
      classprop={"first-letter:text-purple-600"}
      description={`In this project, I worked with a small team to create a banking system app. The app utilizes Next.js Auth for authentication and the Next.js API as the backend. My role in this project was to lead the team, provide solutions, and supervise the team by conducting revisions.`}
      githubLink={"https://github.com/alopez-2018459/bank-app"}
      next
      golang={false}
      typescript
      mongo
    />
    <CardImage image={novaris} />
  </div>
  <h1
    class="font-extrabold montserrat text-9xl max-sm:text-4xl text-center transition-all text-transparent bg-clip-text bg-gradient-to-r from-white to-indigo-500 to-50%"
  >
    BACKEND
  </h1>
  <div
    class="min-h-screen w-full grid grid-cols-2 max-sm:grid-cols-1 grid-flow-row gap-2 mt-10"
  >
    <div
      class="w-full max-sm:hidden min-h-[24rem] max-h-96 text-sky-500 grid place-items-center rounded-md relative overflow-hidden"
    >
      <Icon icon="fa6-brands:golang" width={300} />
    </div>
    <CardText
      title={"Go Field"}
      classprop={"first-letter:text-sky-600"}
      description={`This project is a Golang backend for the "The Field" app. It primarily handles user authentication by storing sessions in a MongoDB database and requires authorization headers. The backend includes features such as protected routes and also includes functionality for creating posts (backend is currently in development for a full migration).`}
      githubLink={"https://github.com/alopez-2018459/go-the-field"}
      next={false}
      golang
      typescript={false}
      mongo
    />

    <CardText
      title={"'Venta Online'"}
      classprop={"first-letter:text-blue-600"}
      description={`This is an Express server made with TypeScript for an e-commerce platform. It encompasses various functionalities including user authentication, role-based authentication, CRUD operations, product management, billing, and cart management. The server is designed to handle these features and facilitate a seamless e-commerce experience.`}
      githubLink={"https://github.com/alopez-2018459/Venta-Online-TypeScript"}
      next={false}
      golang={false}
      typescript
      mongo
    />
    <div
      class="w-full min-h-[24rem] max-sm:hidden max-h-96 text-sky-500 grid place-items-center rounded-md relative overflow-hidden"
    >
      <Icon icon="skill-icons:expressjs-light" width={300} />
    </div>
  </div>
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@600&display=swap");

  .montserrat {
    font-family: "Montserrat", sans-serif;
  }
</style>
