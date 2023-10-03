<script lang="ts">
  import "../app.css";
  import Icon from "@iconify/svelte";
  import { page } from "$app/stores";

  const PAGE_PATH = $page.url.pathname;
  console.log(PAGE_PATH);

  let isOnHome: boolean = true;

  let scrollingY: number;

  if (PAGE_PATH != "/") {
    isOnHome = false;
  }
</script>

<nav
  class=" {isOnHome ? (scrollingY > 40 ? 'opacity-100' : 'opacity-0') : 'opacity-100'}
    fixed inset-x-0 text-xl top-0 py-2 transition-all bg-transparent text-white z-50 px-4 flex justify-end pt-3"
>
  <ul class="flex flex-col items-end gap-2 text-xl mr-20  pb-0 pt-4 bg-black/20 backdrop-blur-sm backdrop-saturate-200
             max-sm:bg-black/70 max-sm:text-white max-sm:p-5 max-sm:w-full max-sm:m-0 max-sm:flex-row">
    <li class="text-sm relative flex items-center gap-1 group/home">
      <div
        class="transition-all group-hover/home:-translate-x-1 flex items-center gap-1 text-gray-400 group-hover/home:text-white"
      >
        <Icon
          icon="pepicons-pop:line-x"
          class="transition-all opacity-0 group-hover/home:opacity-100"
        />
        <a href="/" class="group-hover/home:mr-2">HOME</a>
      </div>
    </li>
    <li class="text-sm relative flex items-center gap-1 group/about">
      <div
        class="transition-all group-hover/about:-translate-x-1 flex items-center gap-1 text-gray-400 group-hover/about:text-white"
      >
        <Icon
          icon="pepicons-pop:line-x"
          class="transition-all opacity-0 group-hover/about:opacity-100"
        />
        <a href="/about" class="group-hover/about:mr-2">ABOUT</a>
      </div>
    </li>
    <li class="text-sm relative flex items-center gap-1 group/projects">
      <div
        class="transition-all group-hover/projects:-translate-x-1 flex items-center gap-1 text-gray-400 group-hover/projects:text-white"
      >
        <Icon
          icon="pepicons-pop:line-x"
          class="transition-all opacity-0 group-hover/projects:opacity-100"
        />

        <a href="/projects" class="group-hover/about:mr-2">PROJECTS</a>
      </div>
    </li>
    <li>
      <a href="https://github.com/ayee-lucas" class="text-white">
        <Icon icon="ant-design:github-filled" />
      </a>
    </li>
    <li>
      <a
        href="https://www.linkedin.com/in/alan-lopez-4a8aa2263"
        class="text-white"
      >
        <Icon icon="mdi:linkedin" />
      </a>
    </li>
  </ul>
</nav>

<slot />

<svelte:window bind:scrollY={scrollingY} />
