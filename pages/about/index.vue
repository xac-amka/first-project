<template>
  <div>
      <ul>
          <li :key="item" v-for="item in 10" style="list-style: none;">
              <h1>
                Support me on Patreon
              </h1>
              <h1 style="color: red;">
                Donate me
              </h1>
          </li>
      </ul>
  </div>
</template>

<script>
export default {
    head() {
        return {
            title: 'About page',
            meta: [
                {
                    hid: 'description',
                    name: 'description',
                    content: 'Best place for learning new words'
                }
            ]
        }
    }
}
</script>

<style>

</style>