<script>
  import checkIcon from '../../assets/pricing/desktop/check.svg';

  let features = [
    {
      title: 'Unlimited Story Posting',
      basic: true,
      pro: true,
      business: true,
    },
    {
      title: 'Unlimited Photo Upload',
      basic: true,
      pro: true,
      business: true,
    },
    {
      title: 'Embedding Custom Content',
      basic: false,
      pro: true,
      business: true,
    },
    {
      title: 'Customize Metadata',
      basic: false,
      pro: true,
      business: true,
    },
    {
      title: 'Advanced Metrics',
      basic: false,
      pro: false,
      business: true,
    },
    {
      title: 'Photo Downloads',
      basic: false,
      pro: false,
      business: true,
    },
    {
      title: 'Search Engine Indexing',
      basic: false,
      pro: false,
      business: true,
    },
    {
      title: 'Custom Analytics',
      basic: false,
      pro: false,
      business: true,
    },
  ];
</script>

<section
  class="hidden flex-col gap-16 px-10 pb-[7rem] pt-14 md:flex xl:gap-14 xl:px-[22.188rem] xl:pb-40 xl:pt-20"
>
  <h2
    class="text-center text-[2.5rem] font-bold uppercase leading-[3rem] tracking-[4.17px] text-pure-black"
  >
    Compare
  </h2>
  <table class="flex flex-col gap-6">
    <thead>
      <tr class="flex w-full border-b border-solid border-pure-black pb-6">
        <th
          class="flex-[2] p-0 text-left text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-black"
          aria-label="The Features">The Features</th
        >
        <th
          class="flex-1 p-0 text-center text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-black"
          aria-label="Basic">Basic</th
        >
        <th
          class="flex-1 p-0 text-center text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-black"
          aria-label="Pro">Pro</th
        >
        <th
          class="flex-1 p-0 text-center text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-black"
          aria-label="Business">Business</th
        >
      </tr>
    </thead>
    <tbody class="flex flex-col gap-6">
      {#each features as feature}
        <tr class="flex w-full border-b border-solid border-[#DFDFDF] pb-6">
          <td
            class="flex-[2] p-0 text-left text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-black"
            aria-label={`${feature.title}`}
          >
            {feature.title}</td
          >
          <td
            class="flex flex-1 items-center justify-center p-0"
            aria-label={`Basic - ${feature.title} - ${
              feature.basic ? 'Enabled' : 'Disabled'
            }`}
            >{#if feature.basic}<div class="h-3 w-4">
                <img
                  class="h-full w-full object-cover"
                  src={checkIcon}
                  alt="check icon"
                />
              </div>{/if}</td
          >
          <td
            class="flex flex-1 items-center justify-center p-0"
            aria-label={`Pro - ${feature.title} - ${
              feature.pro ? 'Enabled' : 'Disabled'
            }`}
            >{#if feature.pro}<div class="h-3 w-4">
                <img
                  class="h-full w-full object-cover"
                  src={checkIcon}
                  alt="check icon"
                />
              </div>{/if}</td
          >
          <td
            class="flex flex-1 items-center justify-center p-0"
            aria-label={`Business - ${feature.title} - ${
              feature.business ? 'Enabled' : 'Disabled'
            }`}
            >{#if feature.business}<div class="h-3 w-4">
                <img
                  class="h-full w-full object-cover"
                  src={checkIcon}
                  alt="check icon"
                />
              </div>{/if}</td
          >
        </tr>
      {/each}
    </tbody>
  </table>
</section>
