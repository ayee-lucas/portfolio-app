<script lang="ts">
  import "animate.css";
  import Icon from "@iconify/svelte";
  import { redirect } from "@sveltejs/kit";

  export let intersecting: boolean;

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

  const handleRedirect = (path:string) => {
    window.location.href = path
  }



</script>

<div
  class="flex items-center justify-center gap-9 w-full mt-10 animate__animated
  bg-gradient-to-r 
  {intersecting ? 'animate__fadeInUp' : 'animate__fadeOutUp'}"
>
  <div
    on:mousemove={(e) => handleOnMouseMove(e)}
    on:click={() => handleRedirect('/projects')}
    aria-hidden
    role="button"
    class="border transition-all border-gray-600 w-52 h-28 max-sm:w-28 grid place-items-center rounded-md text-sm group/cardproject hover:-translate-x-5 relative card"
  >
    <div class="grid place-items-center gap-3">
      <span class="transition-all group-hover/cardproject:text-lg">
        PROJECTS
      </span>
      <Icon
        icon="mingcute:code-line"
        class="transition-all opacity-0 group-hover/cardproject:opacity-100 group-hover/cardproject:text-xl"
      />
    </div>
  </div>
  <div
    on:mousemove={(e) => handleOnMouseMove(e)}
    on:click={() => handleRedirect('/about')}
    aria-hidden
    role="button"
    class="border transition-all border-gray-600 w-52 h-28 max-sm:w-28 grid place-items-center rounded-md text-sm group/cardabout hover:translate-x-5 relative card"
  >
    <div class="grid place-items-center gap-3">
      <span class="transition-all group-hover/cardabout:text-lg">
        ABOUT ME
      </span>
      <Icon
        icon="material-symbols:question-mark"
        class="transition-all opacity-0 group-hover/cardabout:opacity-100 group-hover/cardabout:text-xl"
      />
    </div>
  </div>
</div>

<style>
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
</style>
