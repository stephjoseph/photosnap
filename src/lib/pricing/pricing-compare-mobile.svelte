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

<section class="flex w-full flex-col gap-6 px-7 pb-16 pt-8 md:hidden">
  <h2
    class="text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-black"
  >
    The Features
  </h2>
  <div class="h-px w-full bg-pure-black"></div>
  <div class="flex w-full flex-col gap-6">
    {#each features as feature}
      <div
        class="flex w-full flex-col gap-4 border-b border-solid border-light-grey pb-6"
      >
        <h3
          class="text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-black"
        >
          {feature.title}
        </h3>
        <table class="flex flex-col gap-2 pr-12">
          <thead>
            <tr class="flex w-full">
              <th
                class="flex-1 text-left text-[0.625rem] font-bold uppercase leading-[0.813rem] tracking-[1.67px] text-pure-black/50"
                aria-label="Basic">Basic</th
              >
              <th
                class="flex-1 text-left text-[0.625rem] font-bold uppercase leading-[0.813rem] tracking-[1.67px] text-pure-black/50"
                aria-label="Pro">Pro</th
              >
              <th
                class="flex-1 text-left text-[0.625rem] font-bold uppercase leading-[0.813rem] tracking-[1.67px] text-pure-black/50"
                aria-label="Business">Business</th
              >
            </tr>
          </thead>
          <tbody>
            <tr class="flex w-full">
              <td
                class="flex-1 text-left"
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
                class="flex-1 text-left"
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
                class="flex-1 text-left"
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
          </tbody>
        </table>
      </div>
    {/each}
  </div>
</section>
