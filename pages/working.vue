<template>
  <section>
    <Icon />
    <button @click="counter++">Increment {{ counter }}</button>
  </section>
</template>

<script>
import Icon from '../components/Working.svg' // <----------- Working Icon

export default {
  components: {
    Icon
  },
  data () {
    return { counter: 0 }
  }
}
</script>
