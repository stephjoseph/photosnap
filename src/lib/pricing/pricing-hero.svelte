<script>
  import { onMount, onDestroy } from 'svelte';
  import heroImgMobile from '../../assets/pricing/mobile/hero.jpg';
  import heroImgTablet from '../../assets/pricing/tablet/hero.jpg';
  import heroImgDesktop from '../../assets/pricing/desktop/hero.jpg';

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

<section class="flex w-full flex-col md:max-h-[490px] md:flex-row-reverse">
  <div class="w-full md:w-[35.55%] xl:w-[57.64%]">
    <img class="h-full w-full" src={heroImageUrl} alt="hero" />
  </div>
  <div
    class="relative flex w-full flex-col gap-6 bg-pure-black px-7 py-[4.5rem] before:absolute before:left-8 before:top-0 before:block before:h-[0.375rem] before:w-32 before:bg-gradient-to-tr before:from-[#FFC593] before:from-0% before:via-[#BC7198] before:via-[43.29%] before:to-[#5A77FF] before:to-[83.33%] md:w-[64.45%] md:justify-center md:gap-12 md:px-14 md:py-[10.813rem] md:before:left-0 md:before:top-[10.813rem] md:before:h-[9rem] md:before:w-[0.375rem] xl:w-[42.36%] xl:px-28"
  >
    <div class="flex w-full flex-col gap-4 md:gap-5">
      <h1
        class="text-[2rem] font-bold uppercase leading-10 tracking-[3.33px] text-pure-white md:text-[2.5rem] md:leading-[3rem] md:tracking-[4.17px]"
      >
        Pricing
      </h1>
      <p class="text-[0.938rem] font-normal tracking-normal text-pure-white/60">
        Create a your stories, Photosnap is a platform for photographers and
        visual storytellers. It’s the simple way to create and share your
        photos.
      </p>
    </div>
  </div>
</section>
