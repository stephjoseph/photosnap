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
  import featuredImg5Mobile from '../../assets/stories/mobile/world-tour.jpg';
  import featuredImg5Desktop from '../../assets/stories/desktop/world-tour.jpg';
  import featuredImg6Mobile from '../../assets/stories/mobile/unforeseen-corners.jpg';
  import featuredImg6Desktop from '../../assets/stories/desktop/unforeseen-corners.jpg';
  import featuredImg7Mobile from '../../assets/stories/mobile/king-on-africa.jpg';
  import featuredImg7Desktop from '../../assets/stories/desktop/king-on-africa.jpg';
  import featuredImg8Mobile from '../../assets/stories/mobile/trip-to-nowhere.jpg';
  import featuredImg8Desktop from '../../assets/stories/desktop/trip-to-nowhere.jpg';
  import featuredImg9Mobile from '../../assets/stories/mobile/rage-of-the-sea.jpg';
  import featuredImg9Desktop from '../../assets/stories/desktop/rage-of-the-sea.jpg';
  import featuredImg10Mobile from '../../assets/stories/mobile/running-free.jpg';
  import featuredImg10Desktop from '../../assets/stories/desktop/running-free.jpg';
  import featuredImg11Mobile from '../../assets/stories/mobile/behind-the-waves.jpg';
  import featuredImg11Desktop from '../../assets/stories/desktop/behind-the-waves.jpg';
  import featuredImg12Mobile from '../../assets/stories/mobile/calm-waters.jpg';
  import featuredImg12Desktop from '../../assets/stories/desktop/calm-waters.jpg';
  import featuredImg13Mobile from '../../assets/stories/mobile/milky-way.jpg';
  import featuredImg13Desktop from '../../assets/stories/desktop/milky-way.jpg';
  import featuredImg14Mobile from '../../assets/stories/mobile/dark-forest.jpg';
  import featuredImg14Desktop from '../../assets/stories/desktop/dark-forest.jpg';
  import featuredImg15Mobile from '../../assets/stories/mobile/somwarpet.jpg';
  import featuredImg15Desktop from '../../assets/stories/desktop/somwarpet.jpg';
  import featuredImg16Mobile from '../../assets/stories/mobile/land-of-dreams.jpg';
  import featuredImg16Desktop from '../../assets/stories/desktop/land-of-dreams.jpg';

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
      date: 'April 16th 2020',
    },
    {
      title: 'Sunset Cityscapes',
      author: 'Benjamin Cruz',
      image: {
        mobile: featuredImg2Mobile,
        desktop: featuredImg2Desktop,
      },
      date: 'April 14th 2020',
    },
    {
      title: '18 Days Voyage',
      author: 'Alexei Borodin',
      image: {
        mobile: featuredImg3Mobile,
        desktop: featuredImg3Desktop,
      },
      date: 'April 11th 2020',
    },
    {
      title: 'Architecturals',
      author: 'Samantha Brooke',
      image: {
        mobile: featuredImg4Mobile,
        desktop: featuredImg4Desktop,
      },
      date: 'April 9th 2020',
    },
    {
      title: 'World Tour 2019',
      author: 'Timothy Wagner',
      image: {
        mobile: featuredImg5Mobile,
        desktop: featuredImg5Desktop,
      },
      date: 'April 7th 2020',
    },
    {
      title: 'Unforeseen Corners',
      author: 'William Malcolm',
      image: {
        mobile: featuredImg6Mobile,
        desktop: featuredImg6Desktop,
      },
      date: 'April 3rd 2020',
    },
    {
      title: 'King on Africa: Part II',
      author: 'Tim Hillenburg',
      image: {
        mobile: featuredImg7Mobile,
        desktop: featuredImg7Desktop,
      },
      date: 'March 29th 2020',
    },
    {
      title: 'The Trip to Nowhere',
      author: 'Felicia Rourke',
      image: {
        mobile: featuredImg8Mobile,
        desktop: featuredImg8Desktop,
      },
      date: 'March 21st 2020',
    },
    {
      title: 'Rage of The Sea',
      author: 'Mohammed Abdul',
      image: {
        mobile: featuredImg9Mobile,
        desktop: featuredImg9Desktop,
      },
      date: 'March 19th 2020',
    },
    {
      title: 'Running Free',
      author: 'Michelle',
      image: {
        mobile: featuredImg10Mobile,
        desktop: featuredImg10Desktop,
      },
      date: 'March 16th 2020',
    },
    {
      title: 'Behind the Waves',
      author: 'Lamarr Wilson',
      image: {
        mobile: featuredImg11Mobile,
        desktop: featuredImg11Desktop,
      },
      date: 'March 11th 2020',
    },
    {
      title: 'Calm Waters',
      author: 'Samantha Brooke',
      image: {
        mobile: featuredImg12Mobile,
        desktop: featuredImg12Desktop,
      },
      date: 'March 9th 2020',
    },
    {
      title: 'The Milky Way',
      author: 'Benjamin Cruz',
      image: {
        mobile: featuredImg13Mobile,
        desktop: featuredImg13Desktop,
      },
      date: 'March 5th 2020',
    },
    {
      title: 'Night at The Dark Forest',
      author: 'Mohammed Abdul',
      image: {
        mobile: featuredImg14Mobile,
        desktop: featuredImg14Desktop,
      },
      date: 'March 4th 2020',
    },
    {
      title: 'Somwarpet’s Beauty',
      author: 'Michelle',
      image: {
        mobile: featuredImg15Mobile,
        desktop: featuredImg15Desktop,
      },
      date: 'March 1st 2020',
    },
    {
      title: 'Land of Dreams',
      author: 'William Malcolm',
      image: {
        mobile: featuredImg16Mobile,
        desktop: featuredImg16Desktop,
      },
      date: 'February 25th 2020',
    },
  ];
</script>

<section class="w-full">
  <h2 class="invisible absolute -left-[9999px]">Featured Stories</h2>
  <div class="grid w-full grid-cols-1 md:grid-cols-2 xl:grid-cols-4">
    {#each featured as item}
      <div
        class="relative h-[100vw] w-full bg-cover bg-center bg-no-repeat md:h-[65.10vw] xl:h-[34.65vw]"
        style="background-image: url({windowWidth < 768
          ? item.image.mobile
          : item.image.desktop})"
      >
        <div
          class="absolute left-0 top-0 flex h-full w-full flex-col justify-end bg-gradient-to-b from-pure-black/5 to-pure-black/60 px-8 pb-10 md:px-[2.75rem] xl:px-10"
        >
          <div class="flex flex-col gap-1">
            <span
              class="text-[0.813rem] font-normal leading-[1.063rem] tracking-normal text-pure-white"
              >{item.date}</span
            >
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
