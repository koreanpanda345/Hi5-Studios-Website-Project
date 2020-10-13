<template>
  <div class="bg-gray-300 bg-opacity-25">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <div class="flex items-center">
          <div class="flex-shrink-0" />
          <a href="/"><img class="h-10 w-10" src="https://static1.squarespace.com/static/5d1bd082b615f30001fa83b9/t/5f429bd47999cb5b509efd78/1598201153061/?format=1500w"></a>
        </div>
        <div class="hidden md:block">
          <div class="ml-10 flex items-baseline space-x-4">
            <a href="/" class="px-3 py-2 rounded-md text-sm font-medium text-gray-700 hover:text-gray-300 hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Home</a>
            <a href="/about" class="px-3 py-2 rounded-md text-sm font-medium text-gray-700 hover:text-gray-300 hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">About</a>
            <a href="/channels" class="px-3 py-2 rounded-md text-sm font-medium text-gray-700 hover:text-gray-300 hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Our Channels</a>
            <a href="/shop" class="px-3 py-2 rounded-md text-sm font-medium text-gray-700 hover:text-gray-300 hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Shop</a>
            <a href="https://www.reddit.com/r/Hi5StudiosYT/" class="px-3 py-2 rounded-md text-sm font-medium text-gray-700 hover:text-gray-300 hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700"> Hi5 Reddit</a>
          </div>
        </div>
        <div class="-mr-2 flex md:hidden">
          <!-- Mobile Menu Button -->
          <button @click="toggleMobileMenu()" class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-gray-300 focus:bg-gray-700">
            <!-- Menu open: "hidden", Menu closed: "block" -->
            <svg class="block h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
            <!-- Menu open: "block", Menu closed: "hidden" -->
            <svg class="hidden h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>
    </div>
    <!--
      Mobile menu, toggle classes based on menu state.

      Open: "block", closed: "hidden"
    -->
    <div :class="toggle ? 'block md:hidden' : 'hidden md:hidden'">
      <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
        <a href="/" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Home</a>

        <a href="/about" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">About</a>

        <a href="/channels" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Our Channels</a>

        <a href="/shop" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Shop</a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    toggle: false
  }),
  methods: {
    toggleMobileMenu () {
      this.toggle = !this.toggle
    }
  }
}
</script>
