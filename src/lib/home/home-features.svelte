<script>
  import featureIcon1 from '../../assets/features/desktop/responsive.svg';
  import featureIcon2 from '../../assets/features/desktop/no-limit.svg';
  import featureIcon3 from '../../assets/features/desktop/embed.svg';

  let features = [
    {
      icon: featureIcon1,
      title: '100% Responsive',
      description:
        'No matter which the device you’re on, our site is fully responsive and stories look beautiful on any screen.',
    },
    {
      icon: featureIcon2,
      title: 'No Photo Upload Limit',
      description:
        'Our tool has no limits on uploads or bandwidth. Freely upload in bulk and share all of your stories in one go.',
    },
    {
      icon: featureIcon3,
      title: 'Available to Embed',
      description:
        'Embed Tweets, Facebook posts, Instagram media, Vimeo or YouTube videos, Google Maps, and more. ',
    },
  ];
</script>

<section class="flex w-full flex-col gap-14 px-8 py-20">
  <h2 class="invisible absolute -left-[9999px]">Features</h2>
  {#each features as item}
    <div class="flex w-full flex-col items-center gap-12">
      <div class="w-[4.5rem]">
        <img class="w-full object-top" src={item.icon} alt="" />
      </div>
      <div class="flex w-full flex-col gap-4">
        <h3
          class="text-center text-[1.125rem] font-bold leading-[1.563rem] tracking-normal text-pure-black"
        >
          {item.title}
        </h3>
        <p
          class="text-center text-[0.938rem] font-normal leading-[1.563rem] tracking-normal text-pure-black/60"
        >
          {item.description}
        </p>
      </div>
    </div>
  {/each}
</section>
