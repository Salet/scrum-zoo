<template>
  <div>
    <h1>Welcome to Scrum Zoo! Here are the animals:</h1>
    <div v-for="pic in pictures" :key="pic.id">
      <img :src="require(`~/assets/${pic.id}.jpg`)" class="thumb" alt="" />
      <p class="mt-2 text-sm">{{ pic.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pictures: [{ id: 'chill-cat', text: 'Chill Cat' }],
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
