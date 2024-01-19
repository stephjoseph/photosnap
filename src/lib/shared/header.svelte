<script>
  import logo from '../../assets/shared/desktop/logo.svg';
</script>

<header
  class="hidden w-full items-center justify-between px-10 py-4 md:flex xl:px-[10.313rem]"
>
  <a href="/">
    <img src={logo} alt="photosnap logo" />
  </a>
  <nav>
    <ul class="flex items-center gap-9">
      <li>
        <a
          class="text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-black transition-colors hover:text-pure-black/30 active:text-pure-black/30"
          href="/stories">Stories</a
        >
      </li>
      <li>
        <a
          class="text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-black transition-colors hover:text-pure-black/30 active:text-pure-black/30"
          href="/features">Features</a
        >
      </li>
      <li>
        <a
          class="text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-black transition-colors hover:text-pure-black/30 active:text-pure-black/30"
          href="/pricing">Pricing</a
        >
      </li>
    </ul>
  </nav>
  <a
    href="/"
    class="transtion-colors w-40 bg-pure-black py-[0.75rem] text-center text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-white hover:bg-light-grey hover:text-pure-black active:bg-light-grey active:text-pure-black"
    >Get an invite</a
  >
</header>
