<script>
  import { onMount } from "svelte";
  import PhotoSwipeLightbox from "photoswipe/lightbox";
  import "photoswipe/style.css";
  export let galleryID;
  export let images;
  import { Splide, SplideSlide } from "@splidejs/svelte-splide";
  // Default theme
  import "@splidejs/svelte-splide/css";
  onMount(() => {
    let lightbox = new PhotoSwipeLightbox({
      gallery: "#" + galleryID,
      children: "a",
      pswpModule: () => import("photoswipe"),
      padding: { top: 20, bottom: 40, left: 100, right: 100 },
      preload: [1, 4],
      maxWidthToAnimate: 100,
    });
    lightbox.init();


  });
</script>

{#if images.length > 1}
  <div class="pswp-gallery mt-5 " id={galleryID}>
    <Splide
      options={{
        type: "loop",
        perPage: 4,
        perMove: 1,
        rewind: true,
        padding: "2rem",
      }}
      aria-label="My Favorite Images"
    >
      {#each images as image}

        <SplideSlide>
            <img class="pb-2" src={image.thumbnailURL} alt="" />
          </SplideSlide>
      {/each}
    </Splide>
  </div>
  {:else}
  <h1 class="text-uppercase text-white mt-5"> 
    Hover over a topic to view images
  </h1>
{/if}
