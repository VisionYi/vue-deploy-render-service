<template>
  <div class="about">
    <h1>This is an about page</h1>
    <img width="500" :src="src" alt="src">
  </div>
</template>

<script>
export default {
  name: 'About',
  data () {
    return {
      dog: 'https://images.unsplash.com/photo-1507146426996-ef05306b995a',
      cat: 'https://images.unsplash.com/photo-1514888286974-6c03e2ca1dba',
      src: ''
    }
  },
  created () {
    if (process.env.VUE_APP_PET === 'dog') {
      this.src = this.dog
    } else if (process.env.VUE_APP_PET === 'cat') {
      this.src = this.cat
    }
  }
}
</script>
