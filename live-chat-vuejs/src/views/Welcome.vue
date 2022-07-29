<template>
  <div>
    <h1>{{ title }}</h1>
    <TestComponent message="コンポーネントにデータが渡されている"/>
  </div>
</template>

<script>
import TestComponent from '../components/TestComponent.vue'

export default {
  components: {
    TestComponent
  },
  data() {
    return {
      title: '初めてのvue',
      subtitle: 'ようこそ',
      isEnabled: true
    }
  },
  computed: {
    text() {
      if (this.isEnabled) {
        return 'こんにちは'
      } else {
        return 'さようなら'
      }
    }
  },
  methods: {
    toggle() {
      this.isEnabled = !this.isEnabled
    }
  }
}
</script>