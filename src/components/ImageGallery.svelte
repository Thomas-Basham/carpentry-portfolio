<script>
  export let galleryID;
  export let images;

  import { Splide, SplideSlide } from "@splidejs/svelte-splide";
  // Default theme
  import "@splidejs/svelte-splide/css";
</script>

{#if images.length > 1}
  <Splide
    class="pswp-gallery mt-5 "
    id={galleryID}
    options={{
      slidesPerView: "auto",
      type: "loop",
      autoWidth: true,
      perMove: 1,
      rewind: true,
      padding: "1rem",
      gap: "1rem",
      drag: true,
      lazyLoad: true,
    }}
    aria-label="Project Images"
  >
    {#each images as image}
      <SplideSlide>
        <a
          href={image.largeURL}
          data-pswp-width={image.width}
          data-pswp-height={image.height}
          target="_blank"
          rel="noreferrer"
        >
          <img height="500px" class="splide-image" src={image.largeURL} alt="" />
        </a>
      </SplideSlide>
    {/each}
  </Splide>
{:else}
  <h1 class="text-uppercase text-white mt-5">
    Click a topic to view images
  </h1>
{/if}
