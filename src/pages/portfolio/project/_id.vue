<template>
  <div v-if="project" class="container">
    <h1 class="title">{{ project.title[0].text }}</h1>
  </div>
</template>
<script lang="ts">
import {
  computed,
  defineComponent,
  useAsync,
  useContext,
  useRoute
} from '@nuxtjs/composition-api'

export default defineComponent({
  setup() {
    const route = useRoute()
    const id = route.value.params.id
    const { $prismic } = useContext()

    const getProject = useAsync(async () => {
      return await $prismic.api.query($prismic.predicates.at('document.id', id))
    })

    const project = computed(() => getProject.value?.results[0].data)

    return { project }
  }
})
</script>

<style lang="scss" scoped>
@import '~assets/styles/config';
.container {
  margin: auto;
  margin-top: 2vw;
  width: 80vw;
}
.card-container {
  display: grid;
  gap: 2vw;
  grid-template-columns: 1fr 1fr 1fr;
  margin-top: 2vw;
}
@include tablet {
  .card-container {
    gap: 4vw;
    grid-template-columns: 1fr 1fr;
  }
}
@include mobile-l {
  .card-container {
    gap: 50px;
    grid-template-columns: 1fr;
  }
}
</style>
