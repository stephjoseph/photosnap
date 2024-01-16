<script>
  import { onMount, onDestroy } from 'svelte';
  import heroImgMobile from '../../assets/stories/mobile/moon-of-appalacia.jpg';
  import heroImgTablet from '../../assets/stories/tablet/moon-of-appalacia.jpg';
  import heroImgDesktop from '../../assets/stories/desktop/moon-of-appalacia.jpg';
  import arrow from '../../assets/shared/desktop/arrow-white.svg';

  let windowWidth = 0;

  onMount(() => {
    windowWidth = window.innerWidth;

    window.addEventListener('resize', handleResize);
    return () => {
      window.removeEventListener('resize', handleResize);
    };
  });

  function handleResize() {
    windowWidth = window.innerWidth;
  }

  $: heroImageUrl =
    windowWidth < 768
      ? heroImgMobile
      : windowWidth >= 768 && windowWidth < 1280
        ? heroImgTablet
        : heroImgDesktop;
</script>

<section class="relative flex w-full flex-col">
  <div class="w-full md:max-h-[650px]">
    <img
      class="h-full w-full object-cover object-center"
      src={heroImageUrl}
      alt="hero"
    />
  </div>
  <div
    class="flex w-full flex-col gap-6 bg-pure-black px-7 py-12 md:absolute md:left-0 md:top-0 md:h-full md:justify-center md:bg-transparent md:py-[7.625rem] md:pl-10 md:pr-[21.313rem] xl:pl-[7rem] xl:pr-[58.75rem]"
  >
    <div class="z-10 flex w-full flex-col gap-6">
      <div class="flex w-full flex-col gap-4">
        <span
          class="text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-white md:mb-2"
          >Last month’s featured story</span
        >
        <h1
          class="text-[2rem] font-bold uppercase leading-10 tracking-[3.33px] text-pure-white md:w-4/5 md:text-[2.5rem] md:leading-[3rem] md:tracking-[4.17px]"
        >
          Hazy Full Moon Of Appalachia
        </h1>
        <div class="flex gap-2">
          <span
            class="text-[0.813rem] font-normal leading-[1.063rem] tracking-normal text-pure-white/75"
            >March 2nd 2020</span
          ><span
            class="text-[0.813rem] font-normal leading-[1.063rem] tracking-normal text-pure-white"
            >by John Appleseed</span
          >
        </div>
      </div>
      <p
        class="text-[0.938rem] font-normal leading-[1.563rem] tracking-normal text-pure-white/60"
      >
        The dissected plateau area, while not actually made up of geological
        mountains, is popularly called "mountains," especially in eastern
        Kentucky and West Virginia, and while the ridges are not high, the
        terrain is extremely rugged.
      </p>
    </div>
    <a
      class="peer z-10 flex w-fit items-center gap-[1.125rem] text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-white"
      href="/"
    >
      <span>Read the story</span>
      <img src={arrow} alt="arrow icon" />
    </a>
    <div
      class="invisible left-0 top-0 hidden h-full w-[45rem] bg-[radial-gradient(94.05%_94.05%_at_0%_100%,_#FFC593_0%,_rgba(188,_113,_152,_0.50)_52.36%,_rgba(90,_119,_255,_0.00)_100%)] opacity-0 transition-opacity duration-300 xl:absolute xl:block xl:peer-hover:visible xl:peer-hover:opacity-[0.4899]"
    ></div>
  </div>
</section>
