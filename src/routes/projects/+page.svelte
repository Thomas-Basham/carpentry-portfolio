<script>
  import ImageGallery from "../../components/ImageGallery.svelte";

  class galleryTopic {
    constructor(topic, gallery) {
      this.topic = topic;
      this.gallery = gallery;
    }
  }

  let gallery = [
    {
      largeURL: "",
      thumbnailURL: "",
      width: 0,
      height: 0,
    },
  ];
  const images = [
    {
      largeURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-2500.jpg",
      thumbnailURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-200.jpg",
      width: 2500,
      height: 1666,
    },
    {
      largeURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-2500.jpg",
      thumbnailURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-200.jpg",
      width: 2500,
      height: 1666,
    },
    {
      largeURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-2500.jpg",
      thumbnailURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-200.jpg",
      width: 2500,
      height: 1666,
    },
    {
      largeURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-2500.jpg",
      thumbnailURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-200.jpg",
      width: 2500,
      height: 1666,
    },
    {
      largeURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-2500.jpg",
      thumbnailURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-200.jpg",
      width: 2500,
      height: 1666,
    },
    {
      largeURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-2500.jpg",
      thumbnailURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-200.jpg",
      width: 2500,
      height: 1666,
    },
    {
      largeURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-2500.jpg",
      thumbnailURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-200.jpg",
      width: 2500,
      height: 1666,
    },
    {
      largeURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-2500.jpg",
      thumbnailURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-200.jpg",
      width: 2500,
      height: 1666,
    },
    {
      largeURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-2500.jpg",
      thumbnailURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-200.jpg",
      width: 2500,
      height: 1666,
    },
    {
      largeURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-2500.jpg",
      thumbnailURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-200.jpg",
      width: 2500,
      height: 1666,
    },
    {
      largeURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-2500.jpg",
      thumbnailURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-200.jpg",
      width: 2500,
      height: 1666,
    },
    {
      largeURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-2500.jpg",
      thumbnailURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-200.jpg",
      width: 2500,
      height: 1666,
    },
    {
      largeURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-2500.jpg",
      thumbnailURL:
        "https://cdn.photoswipe.com/photoswipe-demo-images/photos/3/img-200.jpg",
      width: 2500,
      height: 1666,
    },
  ];

  const galleryTopics = [
    new galleryTopic("closets", images),
    new galleryTopic("sheds", images),
    new galleryTopic("remodels", images),
    new galleryTopic("cabinets", images),
  ];
  function setGallery(newGal) {
    gallery = newGal;
  }
</script>

<div class="container mt-5 text-center gallery-container">
  <div class="row gallery-slector">
    {#each galleryTopics as topic}
      <div on:click={() => setGallery(topic.gallery)} class="border col text-white text-uppercase">
        <h1>{topic.topic}</h1>
      </div>
    {/each}
  </div>
</div>
<div class="right-space">
  <ImageGallery galleryID="projects" images={gallery} />
</div>
