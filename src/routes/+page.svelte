<script>
  import HomeHero from '$lib/home/home-hero.svelte';
  import HomeShowcase from '../lib/home/home-showcase.svelte';
  import HomeFeatured from '../lib/home/home-featured.svelte';
  import HomeFeatures from '../lib/home/home-features.svelte';
  import showcaseImg1Mobile from '../assets/home/mobile/beautiful-stories.jpg';
  import showcaseImg1Tablet from '../assets/home/tablet/beautiful-stories.jpg';
  import showcaseImg1Desktop from '../assets/home/desktop/beautiful-stories.jpg';
  import showcaseImg2Mobile from '../assets/home/mobile/designed-for-everyone.jpg';
  import showcaseImg2Tablet from '../assets/home/tablet/designed-for-everyone.jpg';
  import showcaseImg2Desktop from '../assets/home/desktop/designed-for-everyone.jpg';

  let showcase1 = {
    title: 'Beautiful stories every time',
    description:
      'We provide design templates to ensure your stories look terrific. Easily add photos, text, embed maps and media from other networks. Then share your story with everyone.',
    cta: 'View the stories',
    image: {
      mobile: showcaseImg1Mobile,
      tablet: showcaseImg1Tablet,
      desktop: showcaseImg1Desktop,
      position: 'right',
    },
  };

  let showcase2 = {
    title: 'Designed for everyone',
    description:
      'Photosnap can help you create stories that resonate with your audience.  Our tool is designed for photographers of all levels, brands, businesses you name it.',
    cta: 'View the stories',
    image: {
      mobile: showcaseImg2Mobile,
      tablet: showcaseImg2Tablet,
      desktop: showcaseImg2Desktop,
      position: 'right',
    },
  };
</script>

<svelte:head>
  <title>Photosnap - Home</title>
</svelte:head>

<main class="mt-[4.5rem]">
  <HomeHero />
  <HomeShowcase showcase={showcase1} />
  <HomeShowcase showcase={showcase2} />
  <HomeFeatured />
  <HomeFeatures />
</main>
