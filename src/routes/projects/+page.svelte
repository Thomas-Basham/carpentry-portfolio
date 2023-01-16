<script>
  import ImageGallery from "../../components/ImageGallery.svelte";
  import PhotoSwipeLightbox from "photoswipe/lightbox";
  import "photoswipe/style.css";
  import { galleryTopics } from "../../components/images";

  let gallery = [];

  function setGallery(newGal) {
    gallery = newGal;
    let lightbox = new PhotoSwipeLightbox({
      gallery: "#" + "projects",
      children: "a",
      pswpModule: () => import("photoswipe"),
      padding: { top: 20, bottom: 40, left: 100, right: 100 },
      preload: [1, 4],
      maxWidthToAnimate: 100,
    });
    lightbox.init();
  }
</script>

<div class="container mt-5 text-center gallery-container">
  <div class="row gallery-slector">
    {#each galleryTopics as topic}
      <div
        on:onclick={() => setGallery(topic.gallery)}
        on:keydown={() => setGallery(topic.gallery)}
        on:mouseover={() => setGallery(topic.gallery)}
        on:focus={() => setGallery(topic.gallery)}
        class="border col text-white  topic-div pt-2"
      >
        <h1 class="text-uppercase">{topic.topic}</h1>
        <p class="pt-2">
          {topic.description}
        </p>
      </div>
    {/each}
  </div>
</div>
<div class="right-space">
  <ImageGallery galleryID="projects" images={gallery} />
</div>
