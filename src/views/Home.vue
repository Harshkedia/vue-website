<template>
  <div class="home">
    <TextViewer></TextViewer>
  </div>
</template>

<script>
// @ is an alias to /src
import TextViewer from '@/components/TextViewer.vue'

export default {
  name: 'Home',
  components: {
    TextViewer
  },
}
</script>
