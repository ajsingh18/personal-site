<template>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <div class="section section-primary about-section main-header">
    <div class="section-content">
      <h1 class="heading-accent">About Me</h1>
      <p>
        Welcome to my website! I’m Ajay Singh, an experienced IT professional based in Edmonton, AB,
        specializing in web development, custom PC builds, and IT consulting. With over 5 years of
        experience in the tech industry, I’m passionate about helping individuals and businesses
        optimize their technology. Whether you need a professional website, a high-performance
        custom computer, or expert IT advice, I’ve got you covered. By blending my technical skills
        and customer-first approach, I aim to deliver solutions that make technology work for you.
        Let’s connect and take your tech to the next level!
      </p>
    </div>
  </div>
  <main>
    <div class="section section-primary">
      <div class="section-content">
        <h1 class="heading-accent">Website Development</h1>
        <p>
          I design and build custom websites that are not only visually appealing but also optimized
          for performance and security. Whether you’re a small business looking to establish an
          online presence or an individual needing a personal website, I can create responsive,
          SEO-friendly sites tailored to your unique needs. View my completed projects below to see
          examples of the quality work I deliver. Each project reflects my commitment to
          understanding client needs, ensuring their website not only looks great but also functions
          seamlessly.
        </p>
        <div class="web-projects">
          <imgZoomComp
            :img="sjsImg"
            text="SJSHomes"
            id="sjshomes"
            @hover-comp-click="hoverClickHandler"
          ></imgZoomComp>
        </div>
      </div>
    </div>

    <div class="section section-primary pc-section">
      <div class="section-content">
        <h1 class="heading-accent">Custom PC Builds</h1>
        <p>
          Looking for a computer built specifically for your needs? I offer custom PC builds for
          gaming, productivity, or business use. I work with high-quality components to create
          systems that meet your performance demands and budget, ensuring you get exactly what you
          need from your setup.
        </p>
        <br />
        <p>
          Interested in seeing completed customer builds?
          <a href="https://www.instagram.com/frigidpcs" target="_blank" class="link-accent"
            >View them here on Instagram</a
          >
        </p>
        <div data-aos="fade-up" data-aos-duration="1000" class="pc-images-container">
          <image-display></image-display>
        </div>
      </div>
    </div>

    <div class="section section-primary">
      <div class="section-content">
        <h1 class="heading-accent">IT Consulting & Support</h1>
        <p>
          Need help navigating the tech world? From choosing the right software and hardware to
          troubleshooting issues, my IT consulting services provide reliable, expert advice. I can
          help with system upgrades, optimization, security, and much more.
        </p>
      </div>
    </div>
  </main>
  <div class="section section-primary contact-section main-footer">
    <div class="section-content">
      <h1 class="heading-accent">Contact</h1>
      <a href="mailto:frigidpcs@gmail.com">
        <p>Email: frigidpcs@gmail.com</p>
      </a>
      <a href="tel:+1-587-712-1221">
        <p>Phone: (587) 712-1221</p>
      </a>
    </div>
  </div>
</template>

<script setup lang="ts">
import sjsImg from '/images/sjsImg.svg'
import imgZoomComp from '@/components/img-zoom-component.vue'
import imageDisplay from '@/components/img-display.vue'

const hoverClickHandler = (id: string) => {
  if (id === 'sjshomes') {
    window.open('https://sjshomes.ca/', '_blank')?.focus()
  }
}
</script>

<style scoped>
.section-primary {
  padding: 40px 20px;
}

.about-section {
  background-color: #2f2d2e;
}

.contact-section {
  background-color: #2f2d2e;
  text-align: center;
}

.pc-section {
  background-color: #2f2d2e;
}

.pc-images-container {
  margin-top: 16px;
}

.section-content {
  margin: auto;
}

.web-projects {
  margin-top: 16px;
}

.heading-accent {
  color: #f18f01; /* Carrot Orange for headings */
}

.link-accent {
  color: #99c24d; /* Yellow Green for links */
  text-decoration: none;
  border-bottom: 2px solid #99c24d; /* Underline effect */
  padding-bottom: 2px;
}

.link-accent:hover {
  color: #f18f01; /* Hover effect */
  border-color: #f18f01;
}

ul {
  list-style-type: none;
}

h1 {
  text-align: center;
  font-size: 2.5em;
  margin-bottom: 20px;
}

p {
  font-size: 1.25em;
  line-height: 1.6;
}

@media (max-width: 768px) {
  h1 {
    font-size: 2rem;
  }

  .web-projects {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  p,
  li {
    font-size: 1rem;
  }
}
</style>
