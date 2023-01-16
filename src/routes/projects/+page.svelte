<script
  src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"
  integrity="sha384-w76AqPfDkMBDXo30jS1Sgez6pr3x5MlQ1ZAGC+nuZB+EYdgRZgiwxhTBTkF7CXvN"
  crossorigin="anonymous"
>
  import ImageGallery from "../../components/ImageGallery.svelte";
  import PhotoSwipeLightbox from "photoswipe/lightbox";
  import "photoswipe/style.css";
  class galleryTopic {
    constructor(topic, gallery, description) {
      this.topic = topic;
      this.gallery = gallery;
      this.description = description;
    }
  }

  let gallery = [];

  const closetImages = [
    {
      largeURL: "/images/closets/IMG_2.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_3.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_4.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/closets/IMG_5.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_6.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/closets/IMG_7.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/closets/IMG_8.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_9.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_10.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_11.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_12.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_13.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_14.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_15.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_16.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/closets/IMG_17.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/closets/IMG_18.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_19.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/closets/IMG_20.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/closets/IMG_21.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/closets/IMG_22.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/closets/IMG_23.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/closets/IMG_24.jpeg",
      width: 4032,
      height: 3024,
    },
  ];

  const shedImages = [
    {
      largeURL: "/images/sheds/IMG_1.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/sheds/IMG_2.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/sheds/IMG_3.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/sheds/IMG_4.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/sheds/IMG_5.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/sheds/IMG_6.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/sheds/IMG_7.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/sheds/IMG_8.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/sheds/IMG_9.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/sheds/IMG_10.jpeg",
      width: 4032,
      height: 4032,
    },
    {
      largeURL: "/images/sheds/IMG_11.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/sheds/IMG_12.jpeg",
      width: 4032,
      height: 4032,
    },
    {
      largeURL: "/images/sheds/IMG_13.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/sheds/IMG_14.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/sheds/IMG_15.jpeg",
      width: 4032,
      height: 3024,
    },
  ];

  const remodelImages = [
    {
      largeURL: "/images/remodels/IMG_1.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/remodels/IMG_10.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/remodels/IMG_2.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/remodels/IMG_3.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/remodels/IMG_4.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/remodels/IMG_11.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/remodels/IMG_5.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/remodels/IMG_6.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/remodels/IMG_7.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/remodels/IMG_8.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/remodels/IMG_9.jpeg",
      width: 3024,
      height: 4032,
    },
  ];

  const cabinetImages = [
    {
      largeURL: "/images/cabinets/IMG_1.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/cabinets/IMG_2.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/cabinets/IMG_3.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/cabinets/IMG_4.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/cabinets/IMG_5.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/cabinets/IMG_6.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/cabinets/IMG_7.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/cabinets/IMG_8.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/cabinets/IMG_9.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/cabinets/IMG_10.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/cabinets/IMG_11.jpeg",
      width: 4032,
      height: 3024,
    },
  ];

  const windowImages = [
    {
      largeURL: "/images/windows/IMG_1.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/windows/IMG_2.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/windows/IMG_3.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/windows/IMG_4.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/windows/IMG_5.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/windows/IMG_6.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/windows/IMG_7.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/windows/IMG_8.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/windows/IMG_9.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/windows/IMG_10.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/windows/IMG_11.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/windows/IMG_12.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/windows/IMG_13.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/windows/IMG_14.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/windows/IMG_15.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/windows/IMG_16.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/windows/IMG_17.jpeg",
      width: 4032,
      height: 3024,
    },
  ];

  const miscImages = [
    {
      largeURL: "/images/misc/IMG_1.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_2.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_3.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_4.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_5.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_6.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_7.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/misc/IMG_8.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_9.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_10.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_11.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_12.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_13.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_14.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_15.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_16.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_17.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_18.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/misc/IMG_19.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_20.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_21.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/misc/IMG_22.jpeg",
      width: 4032,
      height: 3024,
    },
    {
      largeURL: "/images/misc/IMG_23.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/misc/IMG_24.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/misc/IMG_25.jpeg",
      width: 3024,
      height: 4032,
    },
    {
      largeURL: "/images/misc/IMG_26.jpeg",
      width: 3024,
      height: 4032,
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
      shedImages,
      "I built some of the best sheds money can buy for one of the greatest building company's in America, Old Hickory Buildings and Sheds."
    ),
    new galleryTopic(
      "remodels",
      remodelImages,
      "Passion projects, builds with family/friends, and a desire to make homes look more beautiful."
    ),
    new galleryTopic(
      "cabinets",
      cabinetImages,
      "One of my favorite feelings in the world is transforming someone's old, outdated kitchen into a modern art masterpiece."
    ),
    new galleryTopic(
      "windows",
      windowImages,
      "One of my favorite feelings in the world is transforming someone's old, outdated kitchen into a modern art masterpiece."
    ),
    new galleryTopic(
      "other",
      miscImages,
      "There's not many projects I won't take on. I like to try new thing's and see what happens."
    ),
  ];
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
