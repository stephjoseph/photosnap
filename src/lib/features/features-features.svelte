<script>
  import featureIcon1 from '../../assets/features/desktop/responsive.svg';
  import featureIcon2 from '../../assets/features/desktop/no-limit.svg';
  import featureIcon3 from '../../assets/features/desktop/embed.svg';
  import featureIcon4 from '../../assets/features/desktop/custom-domain.svg';
  import featureIcon5 from '../../assets/features/desktop/boost-exposure.svg';
  import featureIcon6 from '../../assets/features/desktop/drag-drop.svg';

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
        'Embed Tweets, Facebook posts, Instagram media, Vimeo or YouTube videos, Google Maps, and more.',
    },
    {
      icon: featureIcon4,
      title: 'Custom Domain',
      description:
        'With Photosnap subscriptions you can host your stories on your own domain. You can also remove our branding!',
    },
    {
      icon: featureIcon5,
      title: 'Boost Your Exposure',
      description:
        'Users that viewed your story or gallery can easily get notifed of new and featured stories with our built in mailing list.',
    },
    {
      icon: featureIcon6,
      title: 'Drag & Drop Image',
      description:
        'Easily drag and drop your image and get beautiful shots everytime. No over the top tooling to add friction to creating stories.',
    },
  ];
</script>

<section
  class="flex w-full flex-col gap-14 px-8 pb-24 pt-16 md:px-10 md:py-[7rem]"
>
  <h2 class="invisible absolute -left-[9999px]">Features</h2>
  <div
    class="grid w-full grid-cols-1 gap-14 md:grid-cols-2 md:gap-x-3 md:gap-y-[4.5rem]"
  >
    {#each features as item}
      <div class="flex w-full flex-col items-center gap-12">
        <div class="h-[4.5rem] w-[4.5rem]">
          <img
            class="w-full object-top md:object-center"
            src={item.icon}
            alt=""
          />
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
  </div>
</section>
