<template>
  <div>
    <div class="mb-16">
      <nav class="w-full flex items-center justify-between flex-wrap bg-black p-6 rounded-xl">
        <div class="flex items-center flex-shrink-0 text-wh site mr-6">
          <img src="~/assets/cat-ico.png" class="w-12" />
          <NuxtLink to="/">
            <p class="font-semibold text-xl tracking-tight ml-2 text-white">Scrum Zoo</p>
          </NuxtLink>
        </div>
        <div class="block lg:hidden">
          <button
            class="flex items-center px-3 py-2 border rounded text-teal-200 border-teal-400 hover:text-white hover:border-white"
          >
            <svg
              class="fill-current h-3 w-3"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <title>Menu</title>
              <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
            </svg>
          </button>
        </div>
        <div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto">
          <div class="text-sm lg:flex-grow">
            <NuxtLink
              v-for="link in links"
              :key="link.slug"
              :to="link.slug"
              class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4"
            >
              {{ link.title }}
            </NuxtLink>
          </div>
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: [{ slug: '/contact', title: 'Contact' }],
    }
  },
}
</script>
