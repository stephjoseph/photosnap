<script>
  import logoWhite from '../../assets/shared/desktop/logo-white.svg';
  import arrow from '../../assets/shared/desktop/arrow-white.svg';

  // Individual hovered states for each social media icon
  let isFacebookHovered = false;
  let isYoutubeHovered = false;
  let isTwitterHovered = false;
  let isPinterestHovered = false;
  let isInstagramHovered = false;
  let currentYear = new Date().getFullYear();

  const handleMouseOver = (icon) => {
    // Set the hovered state for the corresponding icon
    switch (icon) {
      case 'facebook':
        isFacebookHovered = true;
        break;
      case 'youtube':
        isYoutubeHovered = true;
        break;
      case 'twitter':
        isTwitterHovered = true;
        break;
      case 'pinterest':
        isPinterestHovered = true;
        break;
      case 'instagram':
        isInstagramHovered = true;
        break;
      default:
        break;
    }
  };

  const handleMouseOut = (icon) => {
    // Reset the hovered state for the corresponding icon
    switch (icon) {
      case 'facebook':
        isFacebookHovered = false;
        break;
      case 'youtube':
        isYoutubeHovered = false;
        break;
      case 'twitter':
        isTwitterHovered = false;
        break;
      case 'pinterest':
        isPinterestHovered = false;
        break;
      case 'instagram':
        isInstagramHovered = false;
        break;
      default:
        break;
    }
  };
</script>

<footer
  class="relative hidden w-full flex-col items-center gap-[7.5rem] bg-pure-black px-10 py-16 md:flex xl:px-[10.688rem]"
>
  <div class="flex w-full items-start justify-between">
    <div
      class="flex flex-col gap-8 xl:max-w-[534px] xl:flex-row xl:gap-[6.813rem]"
    >
      <a class="h-4 min-w-[10.625rem]" href="/"
        ><img class="h-full w-full" src={logoWhite} alt="photosnap logo" /></a
      >
      <nav class="z-10 w-full">
        <ul class=" flex w-full min-w-[255px] gap-7 xl:flex-col xl:gap-5">
          <li class="w-full">
            <a
              class="block w-full text-center text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-white transition-colors hover:text-pure-white/30 active:text-pure-white/30 xl:text-left"
              href="/">Home</a
            >
          </li>
          <li class="w-full">
            <a
              class="block w-full text-center text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-white transition-colors hover:text-pure-white/30 active:text-pure-white/30 xl:text-left"
              href="/stories">Stories</a
            >
          </li>
          <li class="w-full">
            <a
              class="block w-full text-center text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-white transition-colors hover:text-pure-white/30 active:text-pure-white/30 xl:text-left"
              href="/features">Features</a
            >
          </li>
          <li class="w-full">
            <a
              class="block w-full text-center text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-white transition-colors hover:text-pure-white/30 active:text-pure-white/30 xl:text-left"
              href="/pricing">Pricing</a
            >
          </li>
        </ul>
      </nav>
    </div>
    <a
      class="group flex items-center justify-center gap-6 text-[0.75rem] font-bold uppercase leading-4 tracking-[2px] text-pure-white"
      href="/"
    >
      <span class="group-hover:underline group-active:underline"
        >Get an invite</span
      >
      <img
        class="transition-transform group-hover:translate-x-1 group-active:translate-x-1"
        src={arrow}
        alt="arrow icon"
      />
    </a>
  </div>
  <div
    class="flex w-full justify-between xl:absolute xl:bottom-16 xl:left-0 xl:px-[10.688rem]"
  >
    <ul class="flex items-center gap-4">
      <li>
        <a href="/">
          <svg
            class="facebook"
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            fill={isFacebookHovered
              ? 'url(#facebook-hover)'
              : 'url(#facebook-normal)'}
            on:mouseover={() => handleMouseOver('facebook')}
            on:mouseout={() => handleMouseOut('facebook')}
            on:focus={() => handleMouseOver('facebook')}
            on:blur={() => handleMouseOut('facebook')}
            role="button"
            tabindex="0"
          >
            <!-- Define gradients for Facebook -->
            <defs>
              <linearGradient
                id="facebook-hover"
                x1="100%"
                x2="0%"
                y1="0%"
                y2="100%"
              >
                <stop offset="0%" stop-color="#63AFDB" />
                <stop offset="100%" stop-color="#6028F1" />
              </linearGradient>
              <linearGradient
                id="facebook-normal"
                x1="100%"
                x2="0%"
                y1="0%"
                y2="100%"
              >
                <stop offset="0%" stop-color="#ffffff" />
                <stop offset="100%" stop-color="#ffffff" />
              </linearGradient>
            </defs>

            <!-- Path for Facebook icon -->
            <path
              fill={isFacebookHovered
                ? 'url(#facebook-hover)'
                : 'url(#facebook-normal)'}
              d="M18.896 0H1.104C.494 0 0 .494 0 1.104v17.793C0 19.506.494 20 1.104 20h9.58v-7.745H8.076V9.237h2.606V7.01c0-2.583 1.578-3.99 3.883-3.99 1.104 0 2.052.082 2.329.119v2.7h-1.598c-1.254 0-1.496.597-1.496 1.47v1.928h2.989l-.39 3.018h-2.6V20h5.098c.608 0 1.102-.494 1.102-1.104V1.104C20 .494 19.506 0 18.896 0z"
            />
          </svg>
        </a>
      </li>
      <li>
        <a href="/">
          <svg
            class="youtube"
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            fill={isYoutubeHovered
              ? 'url(#youtube-hover)'
              : 'url(#youtube-normal)'}
            on:mouseover={() => handleMouseOver('youtube')}
            on:mouseout={() => handleMouseOut('youtube')}
            on:focus={() => handleMouseOver('youtube')}
            on:blur={() => handleMouseOut('youtube')}
            role="button"
            tabindex="0"
          >
            <!-- Define gradients for youtube -->
            <linearGradient id="a" x1="0%" x2="100%" y1="100%" y2="0%"
              ><stop offset="0%" stop-color="#D3205A" /><stop
                offset="100%"
                stop-color="#FF5A5A"
              /></linearGradient
            >
            <defs>
              <linearGradient
                id="youtube-hover"
                x1="0%"
                x2="100%"
                y1="100%"
                y2="0%"
                ><stop offset="0%" stop-color="#D3205A" /><stop
                  offset="100%"
                  stop-color="#FF5A5A"
                /></linearGradient
              >
              <linearGradient
                id="youtube-normal"
                x1="0%"
                x2="100%"
                y1="100%"
                y2="0%"
                ><stop offset="0%" stop-color="#ffffff" /><stop
                  offset="100%"
                  stop-color="#ffffff"
                /></linearGradient
              >
            </defs>

            <!-- Path for youtube icon -->
            <path
              fill={isYoutubeHovered
                ? 'url(#youtube-hover)'
                : 'url(#youtube-normal)'}
              d="M43.33 0c-5.523 0-10 4.478-10 10 0 5.523 4.477 10 10 10s10-4.477 10-10c0-5.522-4.477-10-10-10zm3.7 14.077c-1.75.12-5.653.12-7.402 0-1.896-.13-2.117-1.059-2.131-4.077.014-3.024.237-3.947 2.131-4.077 1.75-.12 5.652-.12 7.403 0 1.897.13 2.117 1.059 2.132 4.077-.015 3.024-.237 3.947-2.132 4.077zm-5.367-6.029l4.098 1.949-4.098 1.955V8.048z"
              transform="translate(-33)"
            />
          </svg>
        </a>
      </li>
      <li>
        <a href="/">
          <svg
            class="twitter"
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            fill={isTwitterHovered
              ? 'url(#twitter-hover)'
              : 'url(#twitter-normal)'}
            on:mouseover={() => handleMouseOver('twitter')}
            on:mouseout={() => handleMouseOut('twitter')}
            on:focus={() => handleMouseOver('twitter')}
            on:blur={() => handleMouseOut('twitter')}
            role="button"
            tabindex="0"
          >
            <!-- Define gradients for twitter -->
            <linearGradient id="a" x1="0%" x2="100%" y1="100%" y2="0%"
              ><stop offset="0%" stop-color="#D3205A" /><stop
                offset="100%"
                stop-color="#FF5A5A"
              /></linearGradient
            >
            <defs>
              <linearGradient
                id="twitter-hover"
                x1="100%"
                x2="0%"
                y1="16.979%"
                y2="83.021%"
                ><stop offset="0%" stop-color="#65FFEB" /><stop
                  offset="100%"
                  stop-color="#27718A"
                /></linearGradient
              >
              <linearGradient
                id="twitter-normal"
                x1="100%"
                x2="0%"
                y1="16.979%"
                y2="83.021%"
                ><stop offset="0%" stop-color="#FFFFFF" /><stop
                  offset="100%"
                  stop-color="#FFFFFF"
                /></linearGradient
              >
            </defs>

            <!-- Path for twitter icon -->
            <path
              fill={isTwitterHovered
                ? 'url(#twitter-hover)'
                : 'url(#twitter-normal)'}
              d="M86.66 3.797a8.192 8.192 0 01-2.357.646 4.11 4.11 0 001.805-2.27 8.22 8.22 0 01-2.606.996 4.096 4.096 0 00-2.995-1.296c-2.65 0-4.596 2.472-3.998 5.038a11.648 11.648 0 01-8.457-4.287 4.109 4.109 0 001.27 5.478 4.086 4.086 0 01-1.858-.513c-.045 1.901 1.318 3.68 3.291 4.075a4.113 4.113 0 01-1.853.07 4.106 4.106 0 003.833 2.85 8.25 8.25 0 01-6.075 1.7 11.616 11.616 0 006.29 1.843c7.618 0 11.922-6.434 11.662-12.205a8.354 8.354 0 002.048-2.124z"
              transform="translate(-66 -1)"
            />
          </svg>
        </a>
      </li>
      <li>
        <a href="/">
          <svg
            class="pinterest"
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            fill={isPinterestHovered
              ? 'url(#pinterest-hover)'
              : 'url(#pinterest-normal)'}
            on:mouseover={() => handleMouseOver('pinterest')}
            on:mouseout={() => handleMouseOut('pinterest')}
            on:focus={() => handleMouseOver('pinterest')}
            on:blur={() => handleMouseOut('pinterest')}
            role="button"
            tabindex="0"
          >
            <!-- Define gradients for pinterest -->
            <linearGradient id="a" x1="0%" x2="100%" y1="100%" y2="0%"
              ><stop offset="0%" stop-color="#D3205A" /><stop
                offset="100%"
                stop-color="#FF5A5A"
              /></linearGradient
            >
            <defs>
              <linearGradient
                id="pinterest-hover"
                x1="100%"
                x2="0%"
                y1="0%"
                y2="100%"
                ><stop offset="0%" stop-color="#F6C683" /><stop
                  offset="100%"
                  stop-color="#DE3838"
                /></linearGradient
              >
              <linearGradient
                id="pinterest-normal"
                x1="100%"
                x2="0%"
                y1="0%"
                y2="100%"
                ><stop offset="0%" stop-color="#FFFFFF" /><stop
                  offset="100%"
                  stop-color="#FFFFFF"
                /></linearGradient
              >
            </defs>

            <!-- Path for pinterest icon -->
            <path
              fill={isPinterestHovered
                ? 'url(#pinterest-hover)'
                : 'url(#pinterest-normal)'}
              d="M109.99 0c-5.522 0-10 4.477-10 10 0 4.237 2.636 7.855 6.356 9.312-.088-.791-.167-2.005.035-2.868.181-.78 1.172-4.97 1.172-4.97s-.299-.6-.299-1.486c0-1.39.806-2.428 1.81-2.428.852 0 1.264.64 1.264 1.408 0 .858-.546 2.14-.828 3.33-.236.995.5 1.807 1.48 1.807 1.778 0 3.144-1.874 3.144-4.58 0-2.393-1.72-4.068-4.176-4.068-2.845 0-4.515 2.135-4.515 4.34 0 .859.33 1.781.744 2.281a.3.3 0 01.069.288l-.278 1.133c-.044.183-.145.223-.335.134-1.249-.581-2.03-2.407-2.03-3.874 0-3.154 2.292-6.052 6.608-6.052 3.469 0 6.165 2.473 6.165 5.776 0 3.447-2.173 6.22-5.19 6.22-1.013 0-1.965-.525-2.291-1.148l-.623 2.378c-.226.869-.835 1.958-1.244 2.621.937.29 1.931.446 2.962.446 5.523 0 10-4.477 10-10s-4.477-10-10-10z"
              transform="translate(-100)"
            />
          </svg>
        </a>
      </li>
      <li>
        <a href="/">
          <svg
            class="instagram"
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            fill={isInstagramHovered
              ? 'url(#instagram-hover)'
              : 'url(#instagram-normal)'}
            on:mouseover={() => handleMouseOver('instagram')}
            on:mouseout={() => handleMouseOut('instagram')}
            on:focus={() => handleMouseOver('instagram')}
            on:blur={() => handleMouseOut('instagram')}
            role="button"
            tabindex="0"
          >
            <!-- Define gradients for instagram -->
            <linearGradient id="a" x1="0%" x2="100%" y1="100%" y2="0%"
              ><stop offset="0%" stop-color="#D3205A" /><stop
                offset="100%"
                stop-color="#FF5A5A"
              /></linearGradient
            >
            <defs>
              <linearGradient
                id="instagram-hover"
                x1="0%"
                x2="50%"
                y1="100%"
                y2="0%"
                ><stop offset="0%" stop-color="#FFC593" /><stop
                  offset="51.945%"
                  stop-color="#BC7198"
                /><stop offset="100%" stop-color="#5A77FF" /></linearGradient
              >
              <linearGradient
                id="instagram-normal"
                x1="0%"
                x2="50%"
                y1="100%"
                y2="0%"
                ><stop offset="0%" stop-color="#FFFFFF" /><stop
                  offset="51.945%"
                  stop-color="#FFFFFF"
                /><stop offset="100%" stop-color="#FFFFFF" /></linearGradient
              >
            </defs>

            <!-- Path for instagram icon -->
            <path
              fill={isInstagramHovered
                ? 'url(#instagram-hover)'
                : 'url(#instagram-normal)'}
              d="M143.32 1.802c2.67 0 2.987.01 4.042.059 2.71.123 3.976 1.409 4.099 4.099.048 1.054.057 1.37.057 4.04 0 2.672-.01 2.988-.057 4.042-.124 2.687-1.387 3.975-4.1 4.099-1.054.048-1.37.058-4.041.058-2.67 0-2.987-.01-4.04-.058-2.718-.124-3.977-1.416-4.1-4.1-.048-1.054-.058-1.37-.058-4.041 0-2.67.01-2.986.058-4.04.124-2.69 1.387-3.977 4.1-4.1 1.054-.048 1.37-.058 4.04-.058zm0-1.802c-2.716 0-3.056.012-4.123.06-3.631.167-5.65 2.182-5.816 5.817-.05 1.067-.061 1.407-.061 4.123s.012 3.057.06 4.123c.167 3.632 2.182 5.65 5.817 5.817 1.067.048 1.407.06 4.123.06s3.057-.012 4.123-.06c3.629-.167 5.652-2.182 5.816-5.817.05-1.066.061-1.407.061-4.123s-.012-3.056-.06-4.122c-.163-3.629-2.18-5.65-5.816-5.817C146.377.01 146.036 0 143.32 0zm0 4.865a5.135 5.135 0 100 10.27 5.135 5.135 0 000-10.27zm0 8.468a3.333 3.333 0 110-6.666 3.333 3.333 0 010 6.666zm5.338-9.87a1.2 1.2 0 100 2.4 1.2 1.2 0 000-2.4z"
              transform="translate(-133)"
            />
          </svg>
        </a>
      </li>
    </ul>
    <p
      class="text-[0.938rem] font-normal leading-5 tracking-normal text-pure-white/50"
    >
      Copyright {currentYear}. All Rights Reserved
    </p>
  </div>
</footer>

<style>
  svg {
    transition-property: color, background-color, border-color,
      text-decoration-color, fill, stroke;
    transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
    transition-duration: 0.3ms;
  }

  svg.facebook:hover {
    fill: url(#facebook-hover); /* Change this to the id of your new gradient for Facebook */
  }

  svg.youtube:hover {
    fill: url(#youtube-hover); /* Change this to the id of your new gradient for YouTube */
  }

  svg.twitter:hover {
    fill: url(#twitter-hover); /* Change this to the id of your new gradient for Twitter */
  }

  svg.pinterest:hover {
    fill: url(#pinterest-hover); /* Change this to the id of your new gradient for Pinterest */
  }

  svg.instagram:hover {
    fill: url(#instagram-hover); /* Change this to the id of your new gradient for Instagram */
  }
</style>
