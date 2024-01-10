<script>
  import logo from '../../assets/shared/desktop/logo.svg';
</script>

<header class="hidden w-full items-center justify-between px-10 py-4 md:flex">
  <a href="/">
    <img src={logo} alt="photosnap logo" />
  </a>
  <nav>
    <ul class="flex items-center gap-9">
      <li>
        <a
          class="text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-black"
          href="/stories">Stories</a
        >
      </li>
      <li>
        <a
          class="text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-black"
          href="/features">Features</a
        >
      </li>
      <li>
        <a
          class="text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-black"
          href="/pricing">Pricing</a
        >
      </li>
    </ul>
  </nav>
  <a
    href="/"
    class="w-40 bg-pure-black py-[0.75rem] text-center text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-white"
    >Get an invite</a
  >
</header>
