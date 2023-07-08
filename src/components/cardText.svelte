<script lang="ts">
  export let title: string;
  export let classprop: string;
  export let description: string;

  const handleOnMouseMove = (
    e: MouseEvent & {
      currentTarget: EventTarget & HTMLDivElement;
    }
  ) => {
    const { currentTarget: target } = e;

    const rect = target.getBoundingClientRect();

    let x = e.clientX - rect.left;
    let y = e.clientY - rect.top;

    target.style.setProperty("--mouse-x", `${x}px`);
    target.style.setProperty("--mouse-y", `${y}px`);
  };
</script>

<div
  on:mousemove={(e) => handleOnMouseMove(e)}
  aria-hidden
  class="w-full min-h-[24rem] max-h-96 border border-zinc-800 relative card montserrat text-gray-200 poppins p-10"
>
  <h1 class="text-3xl uppercase font-semibold {classprop}">
    {title}
  </h1>
  <p class="mt-8">
    {description}
  </p>
</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;600&display=swap');

  .card {
    background-color: rgba(255, 255, 255, 0.02);
  }

  .card:hover::before {
    opacity: 1;
  }

  .card::before {
    background: radial-gradient(
      800px circle at var(--mouse-x) var(--mouse-y),
      rgba(255, 255, 255, 0.1),
      transparent 40%
    );
    border-radius: inherit;
    content: "";
    height: 100%;
    left: 0px;
    position: absolute;
    top: 0px;
    opacity: 0;
    transition: opacity 500ms;
    width: 100%;
    z-index: 2;
  }

  .poppins {
    font-family: "Poppins", sans-serif;
  }
</style>
