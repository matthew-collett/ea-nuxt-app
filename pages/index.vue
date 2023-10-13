<template>
  <div class="container mx-auto px-4 mt-10">
    <header class="text-center">
      <h1 class="text-4xl mb-6">Nuxt Counter App</h1>
    </header>

    <main>
      <section class="text-center mb-6">
        <h2 class="text-2xl mb-4">Current Count: {{ count }}</h2>
        <button @click="increment" class="bg-blue-500 text-white px-4 py-2 rounded mr-2 hover:bg-blue-700">Increment</button>
        <button @click="decrement" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-700">Decrement</button>
      </section>

      <section class="text-center">
        <nuxt-link to="/counter-status" class="bg-green-500 text-white px-4 py-2 rounded hover:bg-green-700">View Counter Status</nuxt-link>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  computed: {
    count() {
      return this.$store.state.count
    }
  },
  methods: {
    increment() {
      this.$store.commit('increment')
    },
    decrement() {
      this.$store.commit('decrement')
    }
  }
}
</script>
