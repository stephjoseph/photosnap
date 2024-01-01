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

<section class="flex w-full flex-col">
  <div class="w-full">
    <img class="h-full w-full" src={heroImageUrl} alt="hero" />
  </div>
  <div class="flex w-full flex-col gap-6 bg-pure-black py-[4.5rem] pl-8 pr-6">
    <div class="flex w-full flex-col gap-4">
      <h1
        class="text-[2rem] font-bold uppercase leading-10 tracking-[3.33px] text-pure-white"
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
