<script>
  import { fly, fade } from 'svelte/transition';
  import logo from '../../assets/shared/desktop/logo.svg';
  import menu from '../../assets/shared/mobile/menu.svg';
  import close from '../../assets/shared/mobile/close.svg';

  let isMenuOpen = false;

  const toggleMenu = () => {
    isMenuOpen = !isMenuOpen;

    document.body.classList.toggle('overflow-y-hidden', isMenuOpen);
  };
</script>

<header class="fixed left-0 top-0 z-50 w-screen md:hidden">
  <div
    class="relative z-50 flex w-full items-center justify-between bg-pure-white px-6 py-7"
  >
    <a on:click={() => (isMenuOpen = false)} href="/">
      <img src={logo} alt="photosnap logo" />
    </a>
    <button type="button" class="relative h-4 w-5" on:click={toggleMenu}>
      {#if isMenuOpen}
        <img
          src={close}
          alt="close btn"
          class="absolute right-[2px] top-[0.5px]"
          transition:fade={{ duration: 300 }}
        />
      {:else}
        <img
          src={menu}
          alt="menu btn"
          class="absolute right-0 top-[5px]"
          transition:fade={{ duration: 300 }}
        />
      {/if}
    </button>
  </div>

  {#if isMenuOpen}
    <nav
      class="fixed left-0 top-[4.5rem] z-20 flex w-full flex-col gap-5 bg-pure-white p-8"
      transition:fly={{ duration: 300, y: -72, opacity: 0 }}
    >
      <ul
        class="flex w-full flex-col gap-5 border-b border-solid border-pure-black/25 pb-5"
      >
        <li>
          <a
            class="block w-full text-center text-[0.938rem] font-bold uppercase leading-5 tracking-[2.5px] text-pure-black transition-colors hover:text-pure-black/30 active:text-pure-black/30"
            on:click={toggleMenu}
            href="/stories">Stories</a
          >
        </li>
        <li>
          <a
            class="block w-full text-center text-[0.938rem] font-bold uppercase leading-5 tracking-[2.5px] text-pure-black transition-colors hover:text-pure-black/30 active:text-pure-black/30"
            on:click={toggleMenu}
            href="/features">Features</a
          >
        </li>
        <li>
          <a
            class="block w-full text-center text-[0.938rem] font-bold uppercase leading-5 tracking-[2.5px] text-pure-black transition-colors hover:text-pure-black/30 active:text-pure-black/30"
            on:click={toggleMenu}
            href="/pricing">Pricing</a
          >
        </li>
      </ul>
      <button
        class="w-full bg-pure-black py-[0.875rem] text-center text-[0.938rem] font-bold uppercase leading-5 tracking-[2.5px] text-pure-white hover:bg-light-grey hover:text-pure-black active:bg-light-grey active:text-pure-black"
        on:click={toggleMenu}>Get an invite</button
      >
    </nav>
    <!-- overlay -->
    <div
      class="fixed bottom-0 left-0 right-0 top-0 z-10 cursor-default bg-pure-black/50"
      transition:fly={{ duration: 300, opacity: 0 }}
      on:click|self={toggleMenu}
      on:keydown={(e) => e.key === 'Escape' && toggleMenu()}
      role="button"
      tabindex="0"
    ></div>
  {/if}
</header>
