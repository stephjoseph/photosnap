<script>
  let isYearly;
  let plans = [
    {
      title: 'Basic',
      description:
        'Includes basic usage of our platform. Recommended for new and aspiring photographers.',
      price: 19.0,
    },
    {
      title: 'Pro',
      description:
        'More advanced features available. Recommended for photography veterans and professionals.',
      price: 39.0,
    },
    {
      title: 'Business',
      description:
        'Additional features available such as more detailed metrics. Recommended for business owners.',
      price: 99.0,
    },
  ];

  const toggleYearly = () => {
    isYearly = !isYearly;
  };
</script>

<section
  class="relative flex w-full flex-col items-center gap-10 px-7 pb-8 pt-16 md:px-10 md:pb-14 md:pt-[7rem] xl:gap-12 xl:px-[10.313rem] xl:pb-20 xl:pt-[7.5rem]"
>
  <h2 class="invisible absolute -left-[9999px]">Pricing Plans</h2>
  <div class="pricing__switch">
    <span
      class:font-bold={!isYearly}
      class="w-[4.5rem] text-[1.125rem] leading-[1.563rem] tracking-normal text-pure-black"
      >Monthly</span
    >
    <label>
      <input type="checkbox" bind:checked={isYearly} on:click={toggleYearly} />
      <span />
    </label>
    <span
      class:font-bold={isYearly}
      class="w-14 text-[1.125rem] leading-[1.563rem] tracking-normal text-pure-black"
      >Yearly</span
    >
  </div>
  <div
    class="flex w-full flex-col gap-6 xl:flex-row xl:items-center xl:gap-[1.875rem]"
  >
    {#each plans as plan, i (plan.title)}
      <div
        class="relative flex w-full flex-col items-center gap-10 px-5 pb-10 pt-14 md:items-start md:gap-8 md:p-10 xl:px-10 {i ===
        1
          ? 'bg-pure-black xl:pb-[4.5rem] xl:pt-[5.5rem]'
          : 'bg-[#F5F5F5] xl:pb-10 xl:pt-14'}"
      >
        {#if i === 1}
          <div
            class="absolute left-0 top-0 block h-[0.375rem] w-full bg-gradient-to-tr from-[#FFC593] from-0% via-[#BC7198] via-[43.29%] to-[#5A77FF] to-[83.33%] md:h-full md:w-[0.375rem] xl:h-[0.375rem] xl:w-full"
          ></div>
        {/if}
        <div
          class="flex w-full flex-col gap-10 md:flex-row md:justify-between xl:flex-col"
        >
          <div
            class="flex flex-col items-center gap-[1.125rem] md:w-[44.41%] md:items-start xl:w-full xl:items-center"
          >
            <h3
              class="text-center text-[1.5rem] font-bold leading-[1.563rem] tracking-normal md:text-left xl:text-center {i ===
              1
                ? 'text-pure-white'
                : 'text-pure-black'}"
            >
              {plan.title}
            </h3>
            <p
              class="text-center text-[0.938rem] font-normal leading-[1.563rem] tracking-normal md:text-left xl:text-center {i ===
              1
                ? 'text-pure-white/60'
                : 'text-pure-black/60'}"
            >
              {plan.description}
            </p>
          </div>
          <div class="flex flex-col items-center">
            <span
              class="text-[2.5rem] font-bold leading-[3rem] tracking-[4.17px] {i ===
              1
                ? 'text-pure-white'
                : 'text-pure-black'}"
              >${isYearly
                ? (plan.price * 10).toFixed(2)
                : plan.price.toFixed(2)}</span
            >
            <span
              class="text-center text-[0.938rem] font-normal leading-[1.563rem] tracking-normal {i ===
              1
                ? 'text-pure-white/60'
                : 'text-pure-black/60'}">per {isYearly ? 'year' : 'month'}</span
            >
          </div>
        </div>
        <a
          class="w-[87.81%] py-3 text-center text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] hover:bg-light-grey hover:text-pure-black md:max-w-[270px] xl:w-full {i ===
          1
            ? 'bg-pure-white text-pure-black'
            : 'bg-pure-black text-pure-white'}"
          href="/">Pick plan</a
        >
      </div>
    {/each}
  </div>
</section>

<style>
  .pricing__switch {
    display: flex;
    align-items: center;
    gap: 32px;
  }

  .pricing__switch label {
    position: relative;
    display: inline-block;
    width: 64px;
    height: 32px;
  }

  .pricing__switch label input {
    opacity: 0;
    width: 0;
    height: 0;
  }

  .pricing__switch label span {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #dfdfdf;
    -webkit-transition: 0.4s;
    transition: 0.4s;
    border-radius: 34px;
  }

  .pricing__switch label span::before {
    position: absolute;
    content: '';
    height: 24px;
    width: 24px;
    left: 4px;
    bottom: 4px;
    background-color: #000000;
    -webkit-transition: 0.4s;
    transition: 0.4s;
    border-radius: 50%;
  }

  .pricing__switch label input:checked + span:before {
    -webkit-transform: translateX(32px);
    -ms-transform: translateX(32px);
    transform: translateX(32px);
  }
</style>
