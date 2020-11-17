<template>
  <div>
    <h1>Welcome to Scrum Zoo! Here are the animals:</h1>
    <div class="flex">
      <div v-for="pic in pictures" :key="pic.img">
        <img :src="require(`~/assets/${pic.img}`)" class="thumb" alt="" />
        <p class="mt-2 text-sm">{{ pic.text }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pictures: [
        { img: 'chill-cat.jpg', text: 'Chill Cat' },
        { img: 'spider.jpg', text: 'Scorpion Spider' },
        { img: 'tiger.jpg', text: 'Wild Tiger' },
        { img: 'azrael.png', text: 'Azrael Cat' },
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
