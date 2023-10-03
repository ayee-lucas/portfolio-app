<!-- component -->
<link
  rel="stylesheet"
  href="https://demos.creative-tim.com/notus-js/assets/styles/tailwind.css"
/>
<link
  rel="stylesheet"
  href="https://demos.creative-tim.com/notus-js/assets/vendor/@fortawesome/fontawesome-free/css/all.min.css"
/>

<script>
    import me from "$lib/images/me.jpeg"
    import bg from "$lib/images/bgwebp.webp"
    import Skills from "../../components/skills.svelte";
</script>

<main class="profile-page max-h-[90vh]">
  <section class="relative block h-500-px">
    <div
      class="absolute top-0 w-full h-full bg-center bg-cover"

    >
      <span
        id="blackOverlay"
        class="w-full h-full absolute opacity-50 bg-black"
      />
      <img src={bg} alt="">
    </div>
    <div
      class="top-auto bottom-0 left-0 right-0 w-full absolute pointer-events-none overflow-hidden h-70-px"
      style="transform: translateZ(0px)"
    >
      <svg
        class="absolute bottom-0 overflow-hidden"
        xmlns="http://www.w3.org/2000/svg"
        preserveAspectRatio="none"
        version="1.1"
        viewBox="0 0 2560 100"
        x="0"
        y="0"
      >
        <polygon
          class="text-blueGray-200 fill-current"
          points="2560 0 2560 100 0 100"
        />
      </svg>
    </div>
  </section>
  <section class="relative py-16 bg-blueGray-200">
    <div class="container mx-auto px-4">
      <div
        class="relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-xl rounded-lg -mt-64"
      >
        <div class="px-6">
          <div class="flex flex-wrap justify-center">
            <div class="w-full lg:w-3/12 px-4 lg:order-2 flex justify-center">
              <div class="relative">
                <img
                  alt="..."
                  src={me}
                  width="300"
                  height="300"
                  class="shadow-xl rounded-full h-auto align-middle border-none absolute -m-16 -ml-20 lg:-ml-16 max-w-150-px"
                />
              </div>
            </div>
            <div
              class="w-full lg:w-4/12 px-4 lg:order-3 lg:text-right lg:self-center"
            >
              <div class="py-6 px-3 mt-32 sm:mt-0">
                <a
                  href="https://www.linkedin.com/in/alan-lopez-4a8aa2263"
                  class="bg-black active:bg-zinc-600 uppercase text-white font-bold hover:shadow-md shadow text-xs px-4 py-2 rounded outline-none focus:outline-none sm:mr-2 mb-1 ease-linear transition-all duration-150"
                  type="button"
                >
                  Connect
                </a>
              </div>
            </div>

          </div>
          <div class="text-center mt-12">
            <h3
              class="text-4xl font-semibold leading-normal mb-2 text-blueGray-700 mb-2"
            >
              Alan Lopez
            </h3>
            <div
              class="text-sm leading-normal mt-0 mb-2 text-blueGray-400 font-bold uppercase"
            >
              <i class="fas fa-map-marker-alt mr-2 text-lg text-blueGray-400" />
              Guatemala, Ciudad de guatemala
            </div>
            <div class="mb-2 text-blueGray-600 mt-10">
              <i
                class="fas fa-briefcase mr-2 text-lg text-blueGray-400"
              />Web Developer
            </div>
            <div class="mb-2 text-blueGray-600">
              <i
                class="fas fa-university mr-2 text-lg text-blueGray-400"
              />Fundacion Kinal
            </div>
          </div>
          <div class="mt-10 py-10 border-t border-blueGray-200 text-center">
            <div class="flex flex-wrap justify-center">
              <div class="w-full lg:w-9/12 px-4">
                <p class="mb-4 text-lg leading-relaxed text-blueGray-700">
                    As a software/web developer, I am passionate about creating innovative and efficient solutions that make a positive impact.

                    With a strong foundation in programming languages and web technologies, I strive to deliver high-quality software and web applications that meet the needs of clients and users.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</main>
