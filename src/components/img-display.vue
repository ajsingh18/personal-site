<template>
  <div class="image-gallery">
    <div class="image-item" style="--fade-in-delay: 0s">
      <img src="/images/pc1.jpg" alt="Image 1" />
    </div>
    <div class="image-item" style="--fade-in-delay: 0.3s">
      <img src="/images/pc2.jpg" alt="Image 2" />
    </div>
    <div class="image-item" style="--fade-in-delay: 0.5s">
      <img src="/images/pc3.png" alt="Image 3" />
    </div>
    <div class="image-item" style="--fade-in-delay: 0.7s">
      <img src="/images/pc5.png" alt="Image 4" />
    </div>
  </div>
</template>

<style scoped>
/* Container for the image gallery */
.image-gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 20px; /* Adds space between images */
  justify-content: center;
  align-items: center;
  padding: 20px;
}

/* Each image item */
.image-item {
  width: 100%;
  max-width: 600px; /* Set max width for each image */
  position: relative;
  opacity: 0;
  transform: translateY(50px); /* Start the image 50px down */
  animation: fadeInFromBottom 1s ease forwards;
  animation-delay: var(--fade-in-delay); /* Apply a staggered delay */
  border-radius: 10px;
  box-shadow: 0px 4px 10px 0px rgba(153, 194, 77, 0.6); /* Yellow Green shadow */
}

/* Responsive adjustments */
@media (min-width: 768px) {
  .image-item {
    width: calc(50% - 20px); /* Two images per row for tablet-sized devices */
  }
}

@media (min-width: 1024px) {
  .image-item {
    width: calc(33.33% - 20px); /* Three images per row for larger screens */
  }
}

/* Keyframes for the fade-in effect */
@keyframes fadeInFromBottom {
  0% {
    opacity: 0;
    transform: translateY(50px); /* Start 50px below */
  }
  100% {
    opacity: 1;
    transform: translateY(0); /* Fade to the original position */
  }
}

/* Image styling */
.image-item img {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
</style>
