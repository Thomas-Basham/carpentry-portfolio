
<script
src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"
integrity="sha384-w76AqPfDkMBDXo30jS1Sgez6pr3x5MlQ1ZAGC+nuZB+EYdgRZgiwxhTBTkF7CXvN"
crossorigin="anonymous"
>
  import ImageGallery from "../../components/ImageGallery.svelte";

  class galleryTopic {
    constructor(topic, gallery, description) {
      this.topic = topic;
      this.gallery = gallery;
      this.description = description;
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

  const closetImages = [
    {
      largeURL: "/images/closets/IMG_2.jpeg",
      thumbnailURL: "/images/closets/thumbnails/THUMB_2.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_3.jpeg",
      thumbnailURL: "/images/closets/thumbnails/THUMB_3.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_4.jpeg",
      thumbnailURL: "/images/closets/thumbnails/THUMB_4.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/closets/IMG_5.jpeg",
      thumbnailURL: "/images/closets/thumbnails/THUMB_5.jpeg",
      width: 3024,
      height: 4032,
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
    new galleryTopic(
      "closets",
      closetImages,
      "These are high quality custom closets that I installed for The Container Store."
    ),
    new galleryTopic(
      "sheds",
      images,
      "I built some of the best sheds money can buy for one of the greatest building company's in America, Old Hickory Buildings and Sheds."
    ),
    new galleryTopic(
      "remodels",
      images,
      "Passion projects, builds with family/friends, and a desire to make homes look more beautiful."
    ),
    new galleryTopic(
      "cabinets",
      images,
      "One of my favorite feelings in the world is transforming someone's old, outdated kitchen into a modern art masterpiece."
    ),
  ];
  function setGallery(newGal) {
    gallery = newGal;
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
