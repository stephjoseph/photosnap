<script>
  import { onMount, onDestroy } from 'svelte';
  import arrow from '../../assets/shared/desktop/arrow-white.svg';
  import bgImageMobile from '../../assets/shared/mobile/bg-beta.jpg';
  import bgImageTablet from '../../assets/shared/tablet/bg-beta.jpg';
  import bgImageDesktop from '../../assets/shared/desktop/bg-beta.jpg';

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

  $: bgImageUrl =
    windowWidth < 768
      ? bgImageMobile
      : windowWidth >= 768 && windowWidth < 1280
        ? bgImageTablet
        : bgImageDesktop;
</script>

<section
  class="relative flex w-full flex-col gap-6 bg-cover bg-center bg-no-repeat px-8 py-16 before:absolute before:left-8 before:top-0 before:block before:h-[0.375rem] before:w-32 before:bg-gradient-to-tr before:from-[#FFC593] before:from-0% before:via-[#BC7198] before:via-[43.29%] before:to-[#5A77FF] before:to-[83.33%] md:flex-row md:justify-between md:gap-0 md:px-10 md:py-[4.25rem] md:before:left-0 md:before:h-full md:before:w-[0.375rem] xl:px-[10.313rem] xl:py-[4.25rem]"
  style="background-image: url({bgImageUrl})"
>
  <h2
    class="text-[2rem] font-bold uppercase leading-10 tracking-[3.33px] text-pure-white md:w-[58.14%] md:text-[2.5rem] md:leading-[3rem] md:tracking-[4.17px] xl:w-[36.04%]"
  >
    We’re in beta. Get your invite today!
  </h2>
  <a
    class="group flex w-fit items-center gap-[1.125rem] text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-white"
    href="/"
  >
    <span class="group-hover:underline group-active:underline"
      >Get an invite</span
    >
    <img
      class="transition-transform group-hover:translate-x-1 group-active:translate-x-1"
      src={arrow}
      alt="arrow icon"
    />
  </a>
</section>
