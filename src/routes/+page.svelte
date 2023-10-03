<script lang="ts">
  import "animate.css";
  import IntersectionObserver from "svelte-intersection-observer";
  import Cards from "../components/cards.svelte";

  export let scrollingY: number;

  let helloClass = "top-0 opacity-0";

  let handAnimation = "";

  let element: HTMLElement;

  let intersecting: boolean;

  setTimeout(() => {
    helloClass = "top-1/2 opacity-100";
  }, 500);

  setTimeout(() => {
    handAnimation = "animate__bounceIn";
  }, 700);
</script>

<main>
  <IntersectionObserver {element} bind:intersecting threshold={0.4}>
    <div class="w-full min-h-screen dark:bg-black flex flex-col">
      <section
        class="w-full min-h-screen transition-all flex justify-center text-center text-5xl text-white"
      >
        <div
          class="absolute flex items-center gap-2 transition-all {helloClass}"
        >
          <h1>Hello!</h1>
          <span class="animate__animated {handAnimation}">👋</span>
        </div>
        <svg
          class="absolute transition-all bottom-10 animate__animated {scrollingY >
          200
            ? 'animate__fadeOut'
            : 'animate__fadeIn'}"
          xmlns="http://www.w3.org/2000/svg"
          width="35"
          height="35"
          viewBox="0 0 24 24"
          ><path
            fill="currentColor"
            d="m12.75 16.19l2.72-2.72a.75.75 0 1 1 1.06 1.06l-4 4a.75.75 0 0 1-1.06 0l-4-4a.75.75 0 1 1 1.06-1.06l2.72 2.72V6.5a.75.75 0 0 1 1.5 0v9.69Z"
          /></svg
        >
      </section>
      <section
        class="w-full min-h-screen transition-all grid place-items-center text-4xl dark:text-white bg-gradient-to-br from-black via-zinc-950 via-50% to-indigo-900"
        bind:this={element}
      >
        <div>
          <h1
            class="animate__animated {intersecting
              ? 'animate__fadeInUp'
              : 'animate__fadeOutUp'} bg-clip-text max-sm:text-xl max-sm:text-center text-transparent bg-gradient-to-r from-white to-indigo-500"
          >
            My name is Alan and, I am a full stack web developer
          </h1>
          <div class="text-lg mt-5">
            <Cards {intersecting}/>
          </div>
        </div>
      </section>
    </div>
  </IntersectionObserver>
</main>

<svelte:window bind:scrollY={scrollingY} />
