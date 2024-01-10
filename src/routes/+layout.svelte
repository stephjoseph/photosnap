<script>
  import '../app.scss';
  import Footer from '../lib/shared/footer.svelte';
  import Header from '../lib/shared/header.svelte';
  import HeaderMobile from '../lib/shared/header-mobile.svelte';
  import FooterMobile from '../lib/shared/footer-mobile.svelte';
</script>

<HeaderMobile />
<Header />
<slot />
<FooterMobile />
<Footer />
