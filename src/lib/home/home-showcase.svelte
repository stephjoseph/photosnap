<script>
  import { onMount, onDestroy } from 'svelte';
  import arrow from '../../assets/shared/desktop/arrow.svg';

  //   export let imagePosition;
  export let showcase;

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

  $: showcaseImageUrl =
    windowWidth < 768
      ? showcase.image.mobile
      : windowWidth >= 768 && windowWidth < 1280
        ? showcase.image.tablet
        : showcase.image.desktop;
</script>

<section class="flex w-full flex-col">
  <div class="w-full">
    <img class="h-full w-full" src={showcaseImageUrl} alt="hero" />
  </div>
  <div class="flex w-full flex-col gap-6 bg-pure-white py-[4.5rem] pl-8 pr-6">
    <div class="flex w-full flex-col gap-4">
      <h2
        class="text-[2rem] font-bold uppercase leading-10 tracking-[3.33px] text-pure-black"
      >
        {showcase.title}
      </h2>
      <p class="text-[0.938rem] font-normal tracking-normal text-pure-black/60">
        {showcase.description}
      </p>
    </div>
    <a
      class="flex w-fit items-center gap-[1.125rem] text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-black"
      href="/"
    >
      <span>{showcase.cta}</span>
      <img src={arrow} alt="arrow icon" />
    </a>
  </div>
</section>
