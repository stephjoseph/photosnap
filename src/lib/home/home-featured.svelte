<script>
  import { onMount, onDestroy } from 'svelte';
  import arrow from '../../assets/shared/desktop/arrow-white.svg';
  import featuredImg1Mobile from '../../assets/stories/mobile/mountains.jpg';
  import featuredImg1Desktop from '../../assets/stories/desktop/mountains.jpg';
  import featuredImg2Mobile from '../../assets/stories/mobile/cityscapes.jpg';
  import featuredImg2Desktop from '../../assets/stories/desktop/cityscapes.jpg';
  import featuredImg3Mobile from '../../assets/stories/mobile/18-days-voyage.jpg';
  import featuredImg3Desktop from '../../assets/stories/desktop/18-days-voyage.jpg';
  import featuredImg4Mobile from '../../assets/stories/mobile/architecturals.jpg';
  import featuredImg4Desktop from '../../assets/stories/desktop/architecturals.jpg';

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

  let featured = [
    {
      title: 'The Mountains',
      author: 'John Appleseed',
      image: {
        mobile: featuredImg1Mobile,
        desktop: featuredImg1Desktop,
      },
    },
    {
      title: 'Sunset Cityscapes',
      author: 'Benjamin Cruz',
      image: {
        mobile: featuredImg2Mobile,
        desktop: featuredImg2Desktop,
      },
    },
    {
      title: '18 Days Voyage',
      author: 'Alexei Borodin',
      image: {
        mobile: featuredImg3Mobile,
        desktop: featuredImg3Desktop,
      },
    },
    {
      title: 'Architecturals',
      author: 'Samantha Brooke',
      image: {
        mobile: featuredImg4Mobile,
        desktop: featuredImg4Desktop,
      },
    },
  ];
</script>

<section class="w-full">
  <h2 class="invisible absolute -left-[9999px]">Featured Stories</h2>
  <div class="grid w-full grid-cols-1 md:grid-cols-2">
    {#each featured as item}
      <div
        class="relative h-[100vw] w-full bg-cover bg-center bg-no-repeat md:h-[65.10vw]"
        style="background-image: url({windowWidth < 768
          ? item.image.mobile
          : item.image.desktop})"
      >
        <div
          class="absolute left-0 top-0 flex h-full w-full flex-col justify-end bg-gradient-to-b from-pure-black/5 to-pure-black/60 px-8 pb-10 md:px-[2.75rem]"
        >
          <div class="flex flex-col gap-1">
            <h3
              class="text-[1.125rem] font-bold leading-[1.563rem] tracking-normal text-pure-white"
            >
              {item.title}
            </h3>
            <span
              class="text-[0.813rem] font-normal leading-[1.063rem] tracking-normal text-pure-white"
              >by {item.author}</span
            >
          </div>
          <div class="mb-5 mt-4 h-px w-full bg-pure-white/25"></div>
          <div class="flex w-full items-center justify-between">
            <a
              class="text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-white"
              href="/">Read story</a
            >
            <a href="/"> <img src={arrow} alt="arrow icon" /></a>
          </div>
        </div>
      </div>
    {/each}
  </div>
</section>

<!-- markup (zero or more items) goes here -->
