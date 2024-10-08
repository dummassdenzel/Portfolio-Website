<script lang="ts">
  import { onMount } from "svelte";
  import LocomotiveScroll from "locomotive-scroll";
  import Swal from "sweetalert2";

  let locomotiveScroll: any;

  onMount(() => {
    locomotiveScroll = new LocomotiveScroll({
      el: document.querySelector("[data-scroll-container]") as HTMLElement,
      smooth: true,
    });

    return () => {
      if (locomotiveScroll) {
        locomotiveScroll.destroy();
      }
    };
  });

  function scrollToSection(target: any) {
    locomotiveScroll.scrollTo(target, {
      offset: 0,
      duration: 2,
    });
  }
</script>

<div data-scroll-container>
  <!-- Platform Icons -->
  <div class="absolute right-3 top-3 flex gap-1">
    <a href="https://github.com/dummassdenzel"
      ><svg
        class="highlight-hover w-12 h-12 text-gray-800 dark:text-white"
        aria-hidden="true"
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        fill="currentColor"
        viewBox="0 0 24 24"
      >
        <path
          fill-rule="evenodd"
          d="M12.006 2a9.847 9.847 0 0 0-6.484 2.44 10.32 10.32 0 0 0-3.393 6.17 10.48 10.48 0 0 0 1.317 6.955 10.045 10.045 0 0 0 5.4 4.418c.504.095.683-.223.683-.494 0-.245-.01-1.052-.014-1.908-2.78.62-3.366-1.21-3.366-1.21a2.711 2.711 0 0 0-1.11-1.5c-.907-.637.07-.621.07-.621.317.044.62.163.885.346.266.183.487.426.647.71.135.253.318.476.538.655a2.079 2.079 0 0 0 2.37.196c.045-.52.27-1.006.635-1.37-2.219-.259-4.554-1.138-4.554-5.07a4.022 4.022 0 0 1 1.031-2.75 3.77 3.77 0 0 1 .096-2.713s.839-.275 2.749 1.05a9.26 9.26 0 0 1 5.004 0c1.906-1.325 2.74-1.05 2.74-1.05.37.858.406 1.828.101 2.713a4.017 4.017 0 0 1 1.029 2.75c0 3.939-2.339 4.805-4.564 5.058a2.471 2.471 0 0 1 .679 1.897c0 1.372-.012 2.477-.012 2.814 0 .272.18.592.687.492a10.05 10.05 0 0 0 5.388-4.421 10.473 10.473 0 0 0 1.313-6.948 10.32 10.32 0 0 0-3.39-6.165A9.847 9.847 0 0 0 12.007 2Z"
          clip-rule="evenodd"
        />
      </svg></a
    >
    <a href="https://www.instagram.com/dumbassdenzel/"
      ><svg
        class="highlight-hover w-12 h-12 text-gray-800 dark:text-white"
        aria-hidden="true"
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        fill="none"
        viewBox="0 0 24 24"
      >
        <path
          fill="currentColor"
          fill-rule="evenodd"
          d="M3 8a5 5 0 0 1 5-5h8a5 5 0 0 1 5 5v8a5 5 0 0 1-5 5H8a5 5 0 0 1-5-5V8Zm5-3a3 3 0 0 0-3 3v8a3 3 0 0 0 3 3h8a3 3 0 0 0 3-3V8a3 3 0 0 0-3-3H8Zm7.597 2.214a1 1 0 0 1 1-1h.01a1 1 0 1 1 0 2h-.01a1 1 0 0 1-1-1ZM12 9a3 3 0 1 0 0 6 3 3 0 0 0 0-6Zm-5 3a5 5 0 1 1 10 0 5 5 0 0 1-10 0Z"
          clip-rule="evenodd"
        />
      </svg></a
    >
    <a href="https://www.linkedin.com/in/denzel-manz-perez-53b89928b"
      ><svg
        class="highlight-hover w-12 h-12 text-gray-800 dark:text-white"
        aria-hidden="true"
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        fill="currentColor"
        viewBox="0 0 24 24"
      >
        <path
          fill-rule="evenodd"
          d="M12.51 8.796v1.697a3.738 3.738 0 0 1 3.288-1.684c3.455 0 4.202 2.16 4.202 4.97V19.5h-3.2v-5.072c0-1.21-.244-2.766-2.128-2.766-1.827 0-2.139 1.317-2.139 2.676V19.5h-3.19V8.796h3.168ZM7.2 6.106a1.61 1.61 0 0 1-.988 1.483 1.595 1.595 0 0 1-1.743-.348A1.607 1.607 0 0 1 5.6 4.5a1.601 1.601 0 0 1 1.6 1.606Z"
          clip-rule="evenodd"
        />
        <path d="M7.2 8.809H4V19.5h3.2V8.809Z" />
      </svg></a
    >
  </div>

  <!-- Header Graphics -->
  <header class="overflow-hidden h-full">
    <img
      src="/images/bg.png"
      alt=""
      class="background h-[125%] w-[125%] max-sm:h-[275%] max-sm:mt-[550px]"
    />
    <div class="foreground h-full w-full">
      <h1
        data-scroll
        data-scroll-speed="0.2"
        class="font-primary mt-36 text-9xl max-sm:text-6xl font-bold text-shadow text-white"
      >
        Denzel Manz
      </h1>
      <div class="flex justify-center mt-3">
        <p
          data-scroll
          data-scroll-speed="0.2"
          class="font-primary bg-black px-6 text-white text-xl text-shadow"
        >
          Full-Stack Developer, Illustrator, Graphic Designer
        </p>
      </div>
    </div>
  </header>

  <!-- Menu Selections -->
  <section
    class="font-primary relative py-10 px-5 bg-black h-[100vh] rounded-t-2xl z-10 -mt-40"
  >
    <!-- Quote -->
    <div class="mb-6">
      <h1 class="text-white text-center text-xl">
        ❝Nothing <b>ventured</b>, nothing <b>gained</b>.❞
      </h1>
    </div>
    <div class="grid grid-cols-4 gap-2 h-[80vh] z-10">
      <button
        on:click={() => scrollToSection("#about-me")}
        class="col-span-1 max-sm:col-span-2 image-wrapper rounded-lg bg-blue-900 hover:shadow-lg flex justify-center items-center"
      >
        <img
          src="/images/aboutme2.jfif"
          alt="About Me"
          class="image-scale h-[100%] w-[100%]"
        />
        <h1
          class="text-shadow text-white text-xl max-sm:text-lg cursor-pointer font-bold bg-black px-6 pb-1 absolute shadow-lg"
          data-scroll
          data-scroll-speed="0.2"
        >
          About me
        </h1>
      </button>
      <button
        on:click={() => scrollToSection("#portfolio")}
        class="col-span-1 max-sm:col-span-2 image-wrapper rounded-lg bg-blue-900 hover:shadow-lg flex justify-center items-center"
      >
        <img
          src="/images/projects1.png"
          alt="Projects"
          class="image-scale h-[100%] w-[100%]"
        />
        <h1
          class="text-white text-xl max-sm:text-lg cursor-pointer font-bold bg-black px-6 pb-1 absolute shadow-lg"
          data-scroll
          data-scroll-speed="0.2"
        >
          My Portfolio
        </h1>
      </button>
      <button
        on:click={() => scrollToSection("#contacts")}
        class="col-span-1 max-sm:col-span-2 image-wrapper rounded-lg bg-blue-900 hover:shadow-lg flex justify-center items-center"
      >
        <img
          src="/images/contacts1.jfif"
          alt="Contacts"
          class="image-scale h-[120%] w-[120%]"
        />
        <h1
          class="text-white text-xl max-sm:text-lg cursor-pointer font-bold bg-black px-6 pb-1 absolute shadow-lg"
          data-scroll
          data-scroll-speed="0.2"
        >
          Contacts
        </h1>
      </button>
      <button
        on:click={() =>
          Swal.fire({
            title: "Feature coming soon!",
            confirmButtonColor: "black",
          })}
        class="col-span-1 max-sm:col-span-2 image-wrapper rounded-lg bg-blue-900 hover:shadow-lg flex justify-center items-center"
      >
        <img
          src="/images/request1.jfif"
          alt=""
          class="image-scale h-[120%] w-[120%]"
        />
        <h1
          class="text-white text-center text-xl max-sm:text-lg cursor-pointer font-bold bg-black px-6 pb-1 absolute shadow-lg"
          data-scroll
          data-scroll-speed="0.2"
        >
          Request a<br /> Commission
        </h1>
      </button>
    </div>
  </section>

  <!-- About Section -->
  <section
    id="about-me"
    class="font-primary text-white bg-black border-t text-lg border-slate-600 px-20 max-sm:px-5"
  >
    <div data-scroll data-scroll-speed="0.3">
      <h1 class="text-center font-bold text-5xl my-10">About me:</h1>
      <p class="indent-10">
        Hi, my name is <b>Denzel Manz S. Perez</b>. Thank you for visiting my
        website — I made it myself. I am currently studying
        <b>Computer Science</b>
        and I have a wide variety of passions I'm continuously honing, let's go over
        them one by one:
      </p>
      <!-- Full-Stack Developer -->
      <div class="mt-16">
        <li class="font-bold text-2xl my-3">Full-Stack Developer:</li>
        <p class="indent-10">
          I am a <b>Full-Stack Developer</b> — currently specializing in
          <b>Angular</b>
          and
          <b>PHP</b>, but I am also currently exploring other languages and
          frameworks to add to my stack like <b>Express</b>, <b>Svelte</b> and
          <b>MongoDB</b>. Apart from my specializations, here are the other
          Software Development Technologies I am capable of:
        </p>
        <div class="flex flex-wrap justify-center gap-7 my-7">
          <img
            src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/angular/angular-original.svg"
            class="w-16 max-sm:w-[6vh] highlight-hover"
            alt="angular logo"
          />
          <img
            src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg"
            class="w-16 max-sm:w-[6vh] highlight-hover"
            alt="javascript logo"
          />
          <img
            src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg"
            class="w-16 max-sm:w-[6vh] highlight-hover"
            alt="typescript logo"
          />
          <img
            src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg"
            class="w-16 max-sm:w-[6vh] highlight-hover"
            alt="html5 logo"
          />
          <img
            src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg"
            class="w-16 max-sm:w-[6vh] highlight-hover"
            alt="css3 logo"
          />
          <img
            src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg"
            class="w-16 max-sm:w-[6vh] highlight-hover"
            alt="python logo"
          />
          <img
            src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg"
            class="w-16 max-sm:w-[6vh] highlight-hover"
            alt="csharp logo"
          />
          <img
            src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg"
            class="w-16 max-sm:w-[6vh] highlight-hover"
            alt="java logo"
          />
          <img
            src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg"
            class="w-16 max-sm:w-[6vh] highlight-hover"
            alt="php logo"
          />
        </div>
      </div>
      <!-- Illustrator-->
      <div class="mt-16">
        <li class="font-bold text-2xl my-3">Illustrator:</li>
        <p class="indent-10">
          I am also a passionate <b>Digital Illustrator</b> — with a few niche
          artstyles ranging from <b>professional</b> to <b>cartoonic</b>. It's
          something that started as a hobby, into something that I am confident
          to do professionally.<br /><br />
          My art styles include <b>semi-realistic</b>, <b>nime</b>, and
          <b>semi-chibi</b> — and I can do <b>Portraits</b>,
          <b>Merchandise Art</b>, and even <b>Animations</b>. As for the
          software I use, I use Krita
        </p>
      </div>
      <!-- Graphic Design-->
      <div class="mt-16">
        <li class="font-bold text-2xl my-3">Graphic Designer:</li>
        <p class="indent-10">
          I am also a <b>Graphic Designer</b> — specifically, the
          <b>Chief Creatives Officer</b>
          the official <b>AWS Learning Club of Gordon College CCS</b>
          and a <b>Layout Artist</b> at the Official Student Publication Unit of
          Gordon College, <b>The ForeFront</b>.<br /><br />
          I design various graphics such as
          <b>Publication Material, Articles, Banners, Posters, Flyers, </b>and
          many more.<br /><br />
        </p>
      </div>
    </div>
  </section>

  <!-- Portfolio Section -->
  <section
    id="portfolio"
    class="font-primary text-white bg-black border-t text-lg border-slate-600 p-10"
  >
    <h1 class="text-center font-bold text-5xl my-10">My Portfolio:</h1>
    <div class="columns-2 sm:columns-2 lg:columns-5 gap-4 space-y-4">
      <div class="image-wrapper">
        <img
          src="/images/projects1.png"
          alt=""
          class="rounded-lg image-scale bg-white"
        />
      </div>
      <div class="image-wrapper">
        <img
          src="/images/finished-projects/dgl.png"
          alt=""
          class="rounded-lg image-scale bg-white"
        />
      </div>
      <div class="image-wrapper">
        <img
          src="/images/finished-projects/awslc.png"
          alt=""
          class="rounded-lg image-scale bg-white"
        />
      </div>
      <div class="image-wrapper">
        <img
          src="/images/finished-projects/slowpoke.png"
          alt=""
          class="rounded-lg image-scale bg-white"
        />
      </div>
      <div class="image-wrapper">
        <img
          src="/images/finished-projects/flsh.png"
          alt=""
          class="rounded-lg image-scale bg-white"
        />
      </div>

      <div class="image-wrapper">
        <img
          src="/images/finished-projects/stcof.png"
          alt=""
          class="rounded-lg image-scale bg-white"
        />
      </div>
      <div class="image-wrapper">
        <img
          src="/images/bg.png"
          alt=""
          class="rounded-lg image-scale bg-white"
        />
      </div>

      <div class="image-wrapper">
        <img
          src="/images/finished-projects/nse.jpg"
          alt=""
          class="rounded-lg image-scale bg-white"
        />
      </div>

      <div class="image-wrapper">
        <img
          src="/images/finished-projects/bkmrk.png"
          alt=""
          class="rounded-lg image-scale bg-white"
        />
      </div>
    </div>
    <div class="flex justify-center mt-10">
      <div class="bg-white text-black highlight-hover p-2 rounded-lg">
        <a class="max-sm:text-sm" href="https://github.com/dummassdenzel">
          <svg
            class="-mt-1 inline w-12 h-12 text-gray-800 dark:text-white"
            aria-hidden="true"
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            fill="currentColor"
            viewBox="0 0 24 24"
          >
            <path
              fill-rule="evenodd"
              d="M12.006 2a9.847 9.847 0 0 0-6.484 2.44 10.32 10.32 0 0 0-3.393 6.17 10.48 10.48 0 0 0 1.317 6.955 10.045 10.045 0 0 0 5.4 4.418c.504.095.683-.223.683-.494 0-.245-.01-1.052-.014-1.908-2.78.62-3.366-1.21-3.366-1.21a2.711 2.711 0 0 0-1.11-1.5c-.907-.637.07-.621.07-.621.317.044.62.163.885.346.266.183.487.426.647.71.135.253.318.476.538.655a2.079 2.079 0 0 0 2.37.196c.045-.52.27-1.006.635-1.37-2.219-.259-4.554-1.138-4.554-5.07a4.022 4.022 0 0 1 1.031-2.75 3.77 3.77 0 0 1 .096-2.713s.839-.275 2.749 1.05a9.26 9.26 0 0 1 5.004 0c1.906-1.325 2.74-1.05 2.74-1.05.37.858.406 1.828.101 2.713a4.017 4.017 0 0 1 1.029 2.75c0 3.939-2.339 4.805-4.564 5.058a2.471 2.471 0 0 1 .679 1.897c0 1.372-.012 2.477-.012 2.814 0 .272.18.592.687.492a10.05 10.05 0 0 0 5.388-4.421 10.473 10.473 0 0 0 1.313-6.948 10.32 10.32 0 0 0-3.39-6.165A9.847 9.847 0 0 0 12.007 2Z"
              clip-rule="evenodd"
            />
          </svg>
          See my Projects on <b>GitHub</b>!
        </a>
      </div>
    </div>
  </section>

  <!-- Contacts Section -->
  <section
    id="contacts"
    class="font-primary text-white bg-black border-t text-lg border-slate-600 py-20 max-sm:px-5"
  >
    <div data-scroll data-scroll-speed="0.3">
      <h1 class="text-center font-bold text-5xl my-10">Contacts:</h1>
      <div class="space-y-4">
        <h3 class="text-center">
          Have a project or a collaboration in mind? <b
            >I’m always open for new opportunities!</b
          ><br /><br /> Reach me at:
        </h3>

        <div class="flex justify-center">
          <div
            class="bg-white text-black py-2 px-4 rounded-lg flex justify-center items-center highlight-hover"
          >
            <img src="/images/icons/email.png" class="h-[6vh]" alt="" />
            <a
              href="mailto:denzelmanzperez1@gmail.com"
              class="max-sm:text-xs ms-5">denzelmanzperez1@gmail.com</a
            >
          </div>
        </div>
        <div class="flex justify-center">
          <div
            class="bg-white text-black py-2 px-4 rounded-lg flex justify-center items-center highlight-hover"
          >
            <img src="/images/icons/linkedin.png" class="h-[6vh]" alt="" />
            <a
              href="https://www.linkedin.com/in/denzel-manz-perez-53b89928b"
              class=" ms-5"
            >
              LinkedIn
            </a>
          </div>
        </div>
        <div class="flex justify-center">
          <div
            class="bg-white text-black py-2 px-4 rounded-lg flex justify-center items-center highlight-hover"
          >
            <img src="/images/icons/facebook.png" class="h-[6vh]" alt="" />
            <a href="https://www.facebook.com/DumbassDenzel/" class=" ms-5">
              Facebook
            </a>
          </div>
        </div>

        <div class="flex justify-center">
          <div
            class="bg-white text-black py-2 px-4 rounded-lg flex justify-center items-center highlight-hover"
          >
            <img src="/images/icons/instagram.png" class="h-[6vh]" alt="" />
            <a href="https://www.instagram.com/dumbassdenzel/" class=" ms-5">
              Instagram
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</div>

<style>
  [data-scroll-container] {
    height: 100vh;
    perspective: 10px;
  }

  header {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    transform-style: preserve-3d;
    z-index: -1;
    text-align: center;
  }

  .background {
    object-position: center 20%;
  }

  .background,
  .foreground {
    position: absolute;
    object-fit: cover;
    z-index: -1;
  }

  .text-shadow {
    text-shadow: 2px 2px 35px rgba(0, 0, 0, 0.5);
  }

  .image-scale {
    object-fit: cover;
    transition: transform 0.3s ease;
  }

  .image-wrapper {
    overflow: hidden;
  }

  .image-wrapper:hover img {
    transform: scale(1.2);
    cursor: pointer;
  }
</style>
