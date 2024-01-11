<script>
  import { onMount, onDestroy } from 'svelte';
  import heroImgMobile from '../../assets/home/mobile/create-and-share.jpg';
  import heroImgTablet from '../../assets/home/tablet/create-and-share.jpg';
  import heroImgDesktop from '../../assets/home/desktop/create-and-share.jpg';
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

<section class="flex w-full flex-col md:max-h-[650px] md:flex-row-reverse">
  <div class="w-full md:w-[35.55%]">
    <img
      class="h-full w-full object-cover object-center"
      src={heroImageUrl}
      alt="hero"
    />
  </div>
  <div
    class="relative flex w-full flex-col gap-6 bg-pure-black py-[4.5rem] pl-8 pr-6 before:absolute before:left-8 before:top-0 before:block before:h-[0.375rem] before:w-32 before:bg-gradient-to-tr before:from-[#FFC593] before:from-0% before:via-[#BC7198] before:via-[43.29%] before:to-[#5A77FF] before:to-[83.33%] md:w-[64.45%] md:justify-center md:gap-12 md:px-14 md:py-[10.813rem] md:before:left-0 md:before:top-[10.813rem] md:before:h-[19rem] md:before:w-[0.375rem]"
  >
    <div class="flex w-full flex-col gap-4">
      <h1
        class="text-[2rem] font-bold uppercase leading-10 tracking-[3.33px] text-pure-white md:text-[2.5rem] md:leading-[3rem] md:tracking-[4.17px]"
      >
        Create and share your photo stories.
      </h1>
      <p class="text-[0.938rem] font-normal tracking-normal text-pure-white/60">
        Photosnap is a platform for photographers and visual storytellers. We
        make it easy to share photos, tell stories and connect with others.
      </p>
    </div>
    <a
      class="flex w-fit items-center gap-[1.125rem] text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-white"
      href="/"
    >
      <span>Get an invite</span>
      <img src={arrow} alt="arrow icon" />
    </a>
  </div>
</section>
