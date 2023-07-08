<script>
  import CardText from "./cardText.svelte";
  import Icon from "@iconify/svelte";
</script>

<div
  class="w-full min-h-screen px-8 flex flex-col gap-10 bg-gradient-to-b from-black to-indigo-950"
>
  <h1 class="text-white text-4xl">SMALLER PROJECTS</h1>
  <p class="text-gray-200 py-10">
    Learning new technologies and creating things are activities that I
    genuinely love. Throughout my journey, I have worked on several smaller
    projects that have not only helped me learn but also showcase my progress.
    These projects have been instrumental in my continuous learning process,
    allowing me to explore and gain hands-on experience with various
    technologies. They serve as tangible evidence of my growth and development
    in the field.
  </p>

  <div class="w-full flex items-center">
    <CardText
      title={"Portfolio"}
      classprop={"first-letter:text-orange-600"}
      description={`My first app using Svelte with the SvelteKit meta framework was an exciting learning experience. SvelteKit provides a streamlined approach to building web applications, and I utilized its features to develop my project.`}
      githubLink={"https://github.com/alopez-2018459/portfolio-app"}
      next={false}
      golang={false}
      typescript={false}
      mongo={false}
    />

    <div class="text-white w-1/2 grid place-items-center">
      <Icon icon="vscode-icons:file-type-svelte" width={300} />
    </div>
  </div>
  <div class="w-full flex items-center">
    <CardText
      title={"Gestor App"}
      classprop={"first-letter:text-blue-400"}
      description={`I developed an application using the Next.js metaframework for hotel and room management and booking. The application incorporates various features and technologies to provide a comprehensive solution.`}
      githubLink={"https://github.com/alopez-2018459/gestor-app"}
      next
      golang={false}
      typescript
      mongo
    />
    <div class="text-white w-1/2 grid place-items-center">
      <Icon icon="logos:nextjs-icon" width={300} />
    </div>
  </div>
  <div class="w-full flex items-center">
    <CardText
      title={"Blackbox"}
      classprop={"first-letter:text-zinc-600"}
      description={`I developed a visually appealing landing page using Next.js and implemented authentication, CRUD operations, and deployed the project on Vercel for the first time.`}
      githubLink={"https://github.com/alopez-2018459/almacen-app"}
      next
      golang={false}
      typescript={false}
      mongo
    />
    <div class="text-white w-1/2 grid place-items-center">
      <Icon icon="akar-icons:vercel-fill" width={300} />
    </div>
  </div>
  <div class="w-full flex items-center">
    <CardText
      title={"Academic Control"}
      classprop={"first-letter:text-green-600"}
      description={`
        One of my earliest well-developed backends was built using Express.js and JavaScript. The application focuses on academic control, specifically managing students, teachers, and course enrollment (role based authentication)`}
      githubLink={"https://github.com/alopez-2018459/Control-de-Alumnos"}
      next={false}
      golang={false}
      typescript={false}
      mongo={true}
    />

    <div class="text-white w-1/2 grid place-items-center">
      <Icon icon="devicon:nodejs" width={300} />
    </div>
  </div>
</div>
