<template>
  <div class="cont">
    <div>
      <Header />
      <Nuxt />
    </div>
    <div class="px-6 pt-4 pb-2">
      <span
        class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2"
      >
        © Scrum Zoo Corporation 2020, Katowice, Brynów
      </span>
    </div>
  </div>
</template>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto,
    'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background: white;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.cont {
  @apply flex flex-col justify-between min-h-screen py-4 mx-auto;
  max-width: 1200px;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  @apply my-4;
}

h1 {
  @apply text-2xl;
}

h2 {
  @apply text-xl;
}

h3 {
  @apply text-lg;
}
</style>
