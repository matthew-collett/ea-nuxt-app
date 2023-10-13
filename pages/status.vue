<template>
  <div class="container mx-auto px-4 mt-10">
    <header class="text-center mb-6">
      <h1 class="text-4xl">Counter Status</h1>
    </header>

    <main class="text-center">
      <p class="mb-6">The counter from the home page is currently at: {{ count }}</p>
      <nuxt-link to="/" class="bg-green-500 text-white px-4 py-2 rounded hover:bg-green-700">Go Back Home</nuxt-link>
    </main>
  </div>
</template>

<script>
export default {
  computed: {
    count() {
      return this.$store.state.count
    }
  }
}
</script>
