<template>
  <div>
    <h1>Welcome to Scrum Zoo! Here are the animals:</h1>
    <div class="flex">
      <a v-for="pic in pictures" :key="pic.img" :href="pic.link">
        <img :src="require(`~/assets/${pic.img}`)" class="thumb" alt="" />
        <p class="mt-2 text-sm">{{ pic.text }}</p>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pictures: [
        { img: 'chill-cat.jpg', text: 'Chill Cat', link: 'https://chill-cat.netlify.app/' },
        {
          img: 'spider.jpg',
          text: 'Scorpion Spider',
          link: 'https://crimsonred.github.io/index.html',
        },
        { img: 'tiger.jpg', text: 'Wild Tiger', link: 'https://psf-training-pn.github.io/' },
        { img: 'azrael.png', text: 'Azrael Cat', link: 'https://knowing-shadow-talk.glitch.me/' },
      ],
    }
  },
}
</script>

<style scoped>
img {
  @apply rounded-xl inline-block;
}

.thumb {
  @apply mr-4;
  height: 250px;
}
</style>
